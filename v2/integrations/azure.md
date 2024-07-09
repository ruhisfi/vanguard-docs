# Integration: Azure

## Overview

Azure integration allows you to manage users and groups in Azure AD from Entra ID.

### Setup

#### SSO

- TBA

#### SOAR & Mail

1. Register a new application in Entra ID
1. Copy the **Client ID** and **Tenant ID** to the corresponding fields in Vanguard
1. Go to **Certificates & secrets** and add new secret
1. Copy the secret and copy it to the corresponding field in Vanguard
1. Go to **API Permissions** add add the following Graph API permissions:

   - User.ReadWrite.All
   - User.ManageIdentities.All
   - Mail.Send
   - Mail.Read

1. Grant admin consent for the permissions
1. From the Entra ID homepage go to **Roles and administrators**
1. Add assignment for the app to the following roles:

   - Password Administrator
   - Security Administrator

#### Cloud Agent

1. Register a new application in Entra ID
1. Copy the **Client ID** and **Tenant ID** to the corresponding fields in the config file
1. Go to **Certificates & secrets** and add new secret
1. Copy the secret and copy it to the corresponding field in the config file
1. Go to **API Permissions** add add the following Graph API permissions:
   - Directory.Read.All
   - Policy.Read.All
   - AuditLog.Read.All
1. Add the following Office 365 Management API permissions:
   - ActivityFeed.Read
   - ActivityFeed.ReadDlp
1. Grant admin consent for the permissions
