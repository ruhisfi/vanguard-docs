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
| users               | array of [User](/resources/user)                                  | Users of the tenant         |
| agents              | array of [Agent](/resources/agent)                                | Agents of the tenant        |
| playbooks           | array of [Playbook](/resources/playbook)                          | Playbooks of the tenant     |
| flags               | object                                                            | Flags of the tenant         |
| licenses            | object                                                            | Licenses of the tenant      |
| createdAt           | timestamp                                                         | Timestamp of creation       |
| updatedAt           | timestamp                                                         | Timestamp of last update    |
