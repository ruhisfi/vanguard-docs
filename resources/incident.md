# Resource: Incident

## Overview

Incidents are collections of alerts that are related to each other. Incidents can be created manually or automatically from alerts.

## Structure

| Field             | Type                                  | Description                                                                                                                   |
| ----------------- | ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| id                | uuid                                  | ID of the resource                                                                                                            |
| description       | string                                | Description of the incident, the main title                                                                                   |
| details           | string                                | Longer description of the incident                                                                                            |
| severity          | integer                               | Severity of the incident, between 1 and 4                                                                                     |
| assignee          | ?string                               | Email of the assignee. Can be `SOAR` for SOAR, or `null` for unassigned                                                       |
| assigneeName      | ?string                               | Display name of the assignee, only set if assignee is defined                                                                 |
| status            | string                                | Status of the incident, can be `OPEN`, `UNDER_INVESTIGATION`, or `RESOLVED`                                                   |
| resolution        | ?string                               | Resolution of the incident, required if status is `RESOLVED`                                                                  |
| resolutionComment | ?string                               | Optional description about the resolution                                                                                     |
| source            | string                                | Source of the incident                                                                                                        |
| mitreTactic       | string                                | MITRE ATT&CK tactic of the incident                                                                                           |
| mitreTechnique    | string                                | MITRE ATT&CK technique of the incident                                                                                        |
| groupingAllowed   | boolean                               | Whether the incident allows more alerts to be grouped                                                                         |
| excludeFromSLA    | boolean                               | Whether the incident is excluded from SLA calculations                                                                        |
| incidentHash      | string                                | Hash of the incident, used as an identifier in emails etc.                                                                    |
| respondedAt       | ?timestamp                            | Timestamp of when the incident was responded to                                                                               |
| resolvedAt        | ?timestamp                            | Timestamp of when the incident was resolved                                                                                   |
| tags              | array of strings                      | Tags of the incident                                                                                                          |
| soarProcessId     | ?uuid                                 | ID of the SOAR process related to the incident                                                                                |
| soarProcess       | [SOARProcess](/resources/soarprocess) | SOAR Process related to the incident                                                                                          |
| soarStatus        | string                                | Status of the SOAR process, can be `NOT_PROCESSED`, `PENDING`, `EXECUTING_PLAYBOOK`, `WAITING_INPUT`, `FINISHED`, or `FAILED` |
| soarTimeout       | ?timestamp                            | Timestamp of when the SOAR process will timeout and continue to next step / fallback step                                     |
| alerts            | array of [Alerts](/resources/alert)   | Alerts related to the incident                                                                                                |
| tenant            | [Tenant](/resources/tenant)           | Tenant of the incident                                                                                                        |
| tenantId          | uuid                                  | ID of the tenant                                                                                                              |
| createdAt         | timestamp                             | Timestamp of creation                                                                                                         |
| updatedAt         | timestamp                             | Timestamp of last update                                                                                                      |
