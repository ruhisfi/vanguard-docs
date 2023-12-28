# Resource: SOAR Process

## Overview

SOAR Process is automatically created when SOAR starts processing an incident. It contains all the information about the incident, including the playbook actions that were executed, the results of those actions, and the current status of the incident.

## Structure

| Field                   | Type                                             | Description                                                       |
| ----------------------- | ------------------------------------------------ | ----------------------------------------------------------------- |
| id                      | uuid                                             | ID of the resource                                                |
| incident                | [Incident](/resources/incident) object           | Incident                                                          |
| memory                  | object                                           | Memory of the incident stored as key-value object                 |
| playbook                | [Playbook](/resources/playbook) object           | Playbook being executed                                           |
| tenant                  | [Tenant](/resources/tenant) object               | Tenant                                                            |
| playbookId              | uuid                                             | ID of the playbook being executed                                 |
| incidentId              | uuid                                             | ID of the incident                                                |
| tenantId                | uuid                                             | ID of the tenant                                                  |
| currentSoarQuestionStep | ?string                                          | Step ID of the question                                           |
| currentSoarQuestion     | ?string                                          | Question text                                                     |
| currentSoarAnswerMemory | ?string                                          | Answer memory key                                                 |
| currentSoarOptions      | ?array of strings                                | Options for the question                                          |
| processHash             | string                                           | Hash of the SOAR process                                          |
| currentStepId           | ?string                                          | ID of the current step                                            |
| currentStep             | [IPlaybookStep](/resources/iplaybookstep) object | Current step                                                      |
| loopIndex               | integer                                          | Index of the loop                                                 |
| loopCollection          | ?string                                          | Collection of the loop                                            |
| loopCollectionLength    | integer                                          | Length of the loop                                                |
| parentProcessId         | ?uuid                                            | If process is a child of another process, this is the parent's id |
| createdAt               | timestamp                                        | Timestamp of creation                                             |
| updatedAt               | timestamp                                        | Timestamp of last update                                          |
