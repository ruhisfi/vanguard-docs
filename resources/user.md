# Resource: User

## Overview

Users are the people who use the platform. Multiple users can exist with the same email, as the login is done using SSO.
If an email exists in multiple tenants, the user will be able to switch between them.

## Structure

| Field       | Type                        | Description                                                |
| ----------- | --------------------------- | ---------------------------------------------------------- |
| id          | uuid                        | ID of the resource                                         |
| email       | string                      | Email of the user                                          |
| ssoLogin    | string                      | Username that will be used in SSO & linking users together |
| name        | string                      | Name of the user                                           |
| active      | boolean                     | Whether the user is active                                 |
| tenantAdmin | boolean                     | Whether the user is a tenant admin                         |
| globalAdmin | boolean                     | Whether the user is a global admin                         |
| title       | string                      | Title of the user                                          |
| lastLogin   | timestamp                   | Timestamp of last login                                    |
| tenantId    | uuid                        | ID of the tenant                                           |
| tenant      | [Tenant](/resources/tenant) | Tenant                                                     |
| emailHash   | string                      | md5 hash of the email used for the profile picture         |
| createdAt   | timestamp                   | Timestamp of creation                                      |
| updatedAt   | timestamp                   | Timestamp of last update                                   |
