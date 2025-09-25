# Overview

To create a trigger profile, navigate to:

**Everbridge Flow Designer → Global Settings → Trigger Profiles**

---

## Trigger Profile: Incident Tasks

1. Click **New** in the upper-right corner of the page.  
2. Complete the following fields:

   - **Name:** `Incident Tasks`
   - **Credentials:** Select the configured xMatters Credentials for this integration.
   - **Workflow:** Choose the workflow from the populated list  
     *(e.g., ServiceNow (Flow Designer) v2 – Major Incident Workbench)*.
   - **Trigger:** Select the trigger for Incident Tasks  
     *(ServiceNow Record Alerts Incident Task `[incident_task]`)*.
   - **Trigger URL:** Automatically filled once you select a trigger.
   - **Default Alert Priority:** Select a default priority *(e.g., Medium)*.  
     This value will be sent to Flow Designer unless overridden by the integration.
   - **Default Signal Mode (Optional):** Enter a signal mode value.  
     This may be overridden if an incident is created or updated.
   - **Additional Recipients:** Enter one or more users or groups from xMatters or Everbridge who should also receive alerts.  
     *(Separate recipients with commas).*
   - **ServiceNow API User:** Select the ServiceNow user account that Flow Designer will use to send updates back to ServiceNow.

3. Click **Submit** to create the trigger profile.

<img width="2706" height="974" alt="Incident_Task_TriggerProfile" src="https://github.com/user-attachments/assets/4900c7c5-a050-40a6-b41a-39090c30aad5" />

---

## Trigger Profile: Incident Communication Task (sys_email)

1. Click **New** in the upper-right corner of the page.  
2. Complete the following fields:

   - **Name:** `Incident Communication Task (sys_email)`
   - **Credentials:** Select the configured xMatters Credentials for this integration.
   - **Workflow:** Choose the workflow from the populated list  
     *(e.g., ServiceNow (Flow Designer) v2 – Major Incident Workbench)*.
   - **Trigger:** Select the trigger for Incident Tasks  
     *(ServiceNow Record Alerts Incident Task `[sys_email]`)*.
   - **Trigger URL:** Automatically filled once you select a trigger.
   - **Default Alert Priority:** Select a default priority *(e.g., Medium)*.  
     This value will be sent to Flow Designer unless overridden by the integration.
   - **Default Signal Mode (Optional):** Enter a signal mode value.  
     This may be overridden if an incident is created or updated.
   - **Additional Recipients:** Enter one or more users or groups from xMatters or Everbridge who should also receive alerts.  
     *(Separate recipients with commas).*
   - **ServiceNow API User:** Select the ServiceNow user account that Flow Designer will use to send updates back to ServiceNow.

3. Click **Submit** to create the trigger profile.

<img width="2650" height="974" alt="Incident_Communication_Task_TriggerProfile" src="https://github.com/user-attachments/assets/f49ecd55-f003-42a7-af6a-8475c56e94dd" />
