# ServiceNow xMatters Integration v2 Enhancement

## Integration Overview

This enhancement extends the **ServiceNow xMatters Integration v2** by incorporating **ServiceNow Major Incident Management** into the xMatters notification process.  

With this update, notifications can now be triggered not only for **Major Incidents** but also for **Incident Tasks** and **Incident Communication Tasks**, providing greater flexibility in how incidents are communicated and managed.  

---

## Pre-Requisites

- **ServiceNow App Version:** Everbridge Flow Designer  
- **xMatters ServiceNow Integration v2:** Install Instructions  
- **ServiceNow Major Incident Plugin:** Install Instructions  
- **xMatters Account:**  
  - Required. If you don’t have one, sign up before proceeding.  

---

## Files

The following update sets are provided:  

- `ServiceNowMIMBusiness Rules (update XML)`  
- `ServiceNowFlowDesignerv2-MajorIncidentWorkbench.zip`  

---

## How It Works

### Major Incident Integration

- **Triggering Notifications:**  
  - xMatters notifications are created only once a Major Incident is changed to **Proposed** or **Accepted** in ServiceNow.  

- **Non-Triggering States:**  
  - **Cancelled** or **Rejected** Major Incidents will not trigger notifications.  

- **Process Control:**  
  - Ensures only **reviewed and approved Major Incidents** generate notifications, preventing noise from unapproved incidents.  

---

### Incident Task & Communication Task Integration

- **Incident Task:**  
  - Notifications can be triggered when ServiceNow **Incident Tasks** (e.g., investigation, resolution, or follow-up work items) are created or updated **and an assignment group is assigned**.  
  - The trigger profile uses the ServiceNow **Record Alerts Incident Task `[incident_task]`** option in Flow Designer (see screenshot).  

- **Incident Communication Task:**  
  - Notifications can also be triggered for **Incident Communication Tasks** to ensure stakeholders and communication teams are alerted promptly.  
  - These follow a similar trigger profile structure, allowing **separate workflows** for technical responders vs. communication recipients.  

---

## Trigger Profile: Incident Tasks

To create a trigger profile, navigate to:

**Everbridge Flow Designer → Global Settings → Trigger Profiles**

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

