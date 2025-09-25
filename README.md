##Overview

Create a trigger profile, go to Everbridge Flow Designer → Global Settings → Trigger Profiles.

Click New in the upper-right corner of the page, then complete the following fields:
•	Name: Enter the following name for this trigger profile: Incident Tasks
•	Credentials: Select the configured xMatters Credentials for this integration.
•	Workflow: Choose the workflow from the populated list (e.g., ServiceNow (Flow Designer) v2 – Major Incident Workbench).
•	Trigger: Select the specific trigger available for Incident Tasks (ServiceNow Record Alerts Incident Task [incident_task]).
•	Trigger URL: This field is automatically filled once you select a trigger. 
•	Default Alert Priority: Select a default priority (e.g., Medium). This value will be sent to Flow Designer unless overridden by the integration.
•	Default Signal Mode: (Optional) Enter a signal mode value. This may be overridden if an incident is created or updated.
•	Additional Recipients (separate recipients with commas): Enter one or more users or groups from xMatters or Everbridge who should also receive alerts.
•	ServiceNow API User: Select the ServiceNow user account that Flow Designer will use to send updates back to ServiceNow.
Click Submit to create the trigger profile.

Create a trigger profile, go to Everbridge Flow Designer → Global Settings → Trigger Profiles.

Click New in the upper-right corner of the page, then complete the following fields:
•	Name: Enter the following name for this trigger profile: Incident Communication Task (sys_email)
•	Credentials: Select the configured xMatters Credentials for this integration.
•	Workflow: Choose the workflow from the populated list (e.g., ServiceNow (Flow Designer) v2 – Major Incident Workbench).
•	Trigger: Select the specific trigger available for Incident Tasks (ServiceNow Record Alerts Incident Task [sys_email]).
•	Trigger URL: This field is automatically filled once you select a trigger. 
•	Default Alert Priority: Select a default priority (e.g., Medium). This value will be sent to Flow Designer unless overridden by the integration.
•	Default Signal Mode: (Optional) Enter a signal mode value. This may be overridden if an incident is created or updated.
•	Additional Recipients (separate recipients with commas): Enter one or more users or groups from xMatters or Everbridge who should also receive alerts.
•	ServiceNow API User: Select the ServiceNow user account that Flow Designer will use to send updates back to ServiceNow.
Click Submit to create the trigger profile.

