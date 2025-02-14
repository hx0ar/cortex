This playbook reassigns active incidents to the current users on call. It requires shift management to be set up.   The playbook can be run as a job a few minutes after the scheduled shift change time.

Update the playbook input with a different search query if required.  Will branch if there are no incidents that match the query and no users on call. 

Cases will not be assigned to users who defined OOO (by OutOfOffice automation).

## Dependencies
This playbook uses the following sub-playbooks, integrations, and scripts.

### Sub-playbooks
This playbook does not use any sub-playbooks.

### Integrations
This playbook does not use any integrations.

### Scripts
* SearchIncidentsV2
* AssignToNextShiftOOO
* SetGridField

### Commands
* getUsers

## Playbook Inputs
---

| **Name** | **Description** | **Default Value** | **Required** |
| --- | --- | --- | --- |
| IncidentSearchQuery | Query for the incidents to reassign.  Incidents need to be active for this to work. It will not reassign pending incidents.  | -status:closed -category:job -type:"Shift handover"   | Optional |

## Playbook Outputs
---
There are no outputs for this playbook.

## Playbook Image
---
![Assign Active Incidents to Next Shift V2](../doc_files/ShiftManagment_Assign_Active_Incidents_to_Next_Shift.png)
