# Resource: IPlaybookStep

## Overview

IPlaybookStep is an interface for the different types of steps in a playbook.

## Structure

## IPlaybookStep

| Field | Type                                    | Description                                                                                     |
| ----- | --------------------------------------- | ----------------------------------------------------------------------------------------------- |
| id    | string                                  | ID of the resource                                                                              |
| data  | [IPlaybookStepData](#iplaybookstepdata) | Step data                                                                                       |
| type  | string                                  | Type of the step, can be `headerNode`, `stepNode`, `conditionalStepNode`, or `playbookStepNode` |

## IPlaybookStepData

| Field            | Type    | Description                                                     |
| ---------------- | ------- | --------------------------------------------------------------- |
| name?            | string  | Name of the step                                                |
| actionType?      | ?string | Type of the step action                                         |
| isRoot?          | boolean | Whether the step is the root of the playbook                    |
| type?            | ?string | Type of the step, can be `standard`, `conditional`, or `header` |
| parameters?      | ?object | Parameters of the step action                                   |
| ifValue?         | string  | Header for conditional if                                       |
| elseValue?       | string  | Header for conditional else                                     |
| elseIfValue?     | string  | Header for conditional else if                                  |
| ifCondition?     | string  | Condition for conditional if                                    |
| elseIfCondition? | string  | Condition for conditional else                                  |
| subPlaybookId?   | string  | ID of the sub-playbook                                          |
| loopCollection?  | string  | Loop collection                                                 |
| loopVariable?    | string  | Loop variable                                                   |
