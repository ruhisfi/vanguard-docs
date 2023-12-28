# Resource: Alert

## Overview

Alerts are the core of the system. They are created by Correlation Rules, BIOCs, and IOCs. They can be grouped into [incidents](/resources/incident). Most of the fields can be null, because they might not always be available from the alert source.

## Structure

| Field              | Type                             | Description                                          |
| ------------------ | -------------------------------- | ---------------------------------------------------- |
| id                 | uuid                             | ID of the resource                                   |
| ruleName           | string                           | Name of the rule that caused the alert               |
| hostname           | ?string                          | Hostname                                             |
| srcHostname        | ?string                          | Source hostname                                      |
| srcIp              | ?string                          | Source IP                                            |
| srcPort            | ?integer                         | Source port                                          |
| destHostname       | ?string                          | Destination hostname                                 |
| destIp             | ?string                          | Destination IP                                       |
| destPort           | ?integer                         | Destination port                                     |
| username           | ?string                          | Username                                             |
| source             | string                           | Source of the alert                                  |
| action             | string                           | Action of the alert, usually "Detected" or "Blocked" |
| category           | string                           | Category of the alert                                |
| description        | string                           | Description of the alert                             |
| severity           | integer                          | Severity of the alert, between 0 and 4               |
| initiatedBy        | ?string                          | Initiator process name                               |
| initiatorPath      | ?string                          | Initiator process path                               |
| initiatorCmd       | ?string                          | Initiator process command                            |
| initiatorSignature | string                           | Initiator process signature                          |
| initiatorSigner    | ?string                          | Initiator process signer                             |
| initiatorHash      | ?string                          | Initiator process hash                               |
| mitreTactic        | string                           | MITRE ATT&CK tactic of the alert                     |
| mitreTechnique     | string                           | MITRE ATT&CK technique of the alert                  |
| tags               | array of strings                 | Tags of the alert                                    |
| rawEventDataset    | string                           | Raw event dataset of the alert, needed for queries   |
| rawEventId         | string                           | Raw event ID of the alert, needed for queries        |
| incidentId         | ?uuid                            | ID of the incident this alert was grouped to         |
| incident           | ?[Incident](/resources/incident) | Incident this alert was grouped to                   |
| tenant             | [Tenant](/resources/tenant)      | Tenant of the alert                                  |
| tenantId           | uuid                             | ID of the tenant                                     |
| createdAt          | timestamp                        | Timestamp of creation                                |
| updatedAt          | timestamp                        | Timestamp of last update                             |
