# Resource: Playbook

## Overview

Playbooks can be used to automate the response to incidents. They are made up of a series of steps, each of which can be a manual action or an automated action. Playbooks can be triggered automatically by criteria or manually.

## Structure

| Field       | Type                                               | Description                                                     |
| ----------- | -------------------------------------------------- | --------------------------------------------------------------- |
| id          | uuid                                               | ID of the resource                                              |
| name        | string                                             | Name of the playbook                                            |
| description | string                                             | Description of the playbook                                     |
| trigger     | string                                             | Trigger of the playbook, can be `incident`, `email` or `manual` |
| enabled     | boolean                                            | Whether the playbook is enabled                                 |
| criteria    | string                                             | Criteria for when the playbook should be triggered, format: RQL |
| steps       | array of [IPlaybookStep](/resources/iplaybookstep) | Steps of the playbook                                           |
| edges       | array of IPlaybookEdge                             | Edges of the playbook                                           |
| weight      | integer                                            | Weight of the playbook, higher will get evaluated first         |
| tenant      | [Tenant](/resources/tenant)                        | Tenant                                                          |
| tenantId    | uuid                                               | ID of the tenant                                                |
| createdAt   | timestamp                                          | Timestamp of creation                                           |
| updatedAt   | timestamp                                          | Timestamp of last update                                        |
