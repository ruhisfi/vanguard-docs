# Resource: Tenant

## Overview

Tenants are used to separate data between different organizations. Each tenant has its own users, alerts, incidents, playbooks, etc.

## Structure

| Field               | Type                                                              | Description                 |
| ------------------- | ----------------------------------------------------------------- | --------------------------- |
| id                  | uuid                                                              | ID of the resource          |
| name                | string                                                            | Name of the tenant          |
| settings            | [TenantSettings](/resources/tenantsettings)                       | Tenant Settings             |
| integrationSettings | [TenantIntegrationSettings](/resources/tenantintegrationsettings) | Tenant Integration Settings |
| users               | array of [Users](/resources/user)                                 | Users of the tenant         |
| agents              | array of [Agents](/resources/agent)                               | Agents of the tenant        |
| playbooks           | array of [Playbooks](/resources/playbook)                         | Playbooks of the tenant     |
| flags               | [flags](#flags)                                                   | Flags of the tenant         |
| licenses            | object                                                            | Licenses of the tenant      |
| createdAt           | timestamp                                                         | Timestamp of creation       |
| updatedAt           | timestamp                                                         | Timestamp of last update    |

## Flags

| Key       | Value                 | Description                                                                                   |
| --------- | --------------------- | --------------------------------------------------------------------------------------------- |
| suspended | reason for suspension | Whether the tenant is suspended, meaning that no users can log in and data won't be ingested. |
| eval      | expiration date       | Whether the tenant is an evaluation tenant.                                                   |
| demo      | N/A                   | Whether the tenant is a demo tenant.                                                          |
| dev       | N/A                   | Whether the tenant is a development tenant.                                                   |
