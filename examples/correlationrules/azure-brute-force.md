# Azure: Successful Brute Force

## Overview

This correlation rule is designed to detect successful brute force attacks against Office 365 accounts. It will be triggered when a user has a successful login from an IP address that has had failed logins in the past 45 minutes.

## Requirements

- [Azure Integration](/integrations/azure)

## Configuration

- **Severity**: High (Medium if you want to be less aggressive)
- **Timeframe**: 45 minutes
- **Message Template**: `Successful login on user {userPrincipalName} after failed logins`
- **Tags**: `azure,bruteforce`
- **Trigger Query**:
  ```rql
  dataset = msft_signins
  | filter status.errorCode = 0
  ```
- **Correlation Query**:
  ```rql
  dataset = msft_signins
  | filter status.errorCode > 0 and status.errorCode != 50140
  | filter userPrincipalName = "{userPrincipalName}" and ipAddress = "{ipAddress}"
  ```
