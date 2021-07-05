## Objectives:

* Locate lightning app builder header and toolbar buttons
* Deploy org-wide defaults & criteria-based sharing rules together
* Develop flow screen components that work for multiple objects 
* Break up your record details with Dynamic forms
* Debug flow errors in a sandbox org as another user


### Deploy org-wide defaults & criteria-based sharing rules together
* You can now simultaneously update the sharingModel field for an object and create new criteria-based or guest user sharing rules via the Metadata API. 

### Develop flow screen components that work for multiple objects:
* Create re-usable flow screen components that use the **generic sObjects & sObjects[] data types**
This works by building one component that works for multiple objects instead of one component per object.

### Break up your record details with Dynamic forms
Ability to configure record details fields and sections inside the Lightning App Builder.
With Dynamic Forms you can:
* migrate the fields and sections on your page layout as individual components into the Lightning App Builder.

### Debug flow errors in a sandbox org as another user

* Process Automation Settings --> select the Let admins debug flows as other users checkbox
* open a flow in Flow Builder and click Debug
* Select the Run flow as another user checkbox, and choose a user to impersonate.

**Debugging a flow as another user is available only for screen flows and autolaunched flows in nonproduction orgs**
**Any operations performed by screen components are performed as the logged-in user and not as the impersonated user.**


## Update New and Changed Records by Using Before-Save Updates in Flows
**You can trigger a flow to run before a record is saved** (create or update)
**an app builder needs the View All Data permission in order to activate a flow that makes before-save updates**
* Before-save updates in flows accomplish the updates more quickly compared to Process builder record-change process **because each record doesn’t get saved to the database again** (skipping another round of assignment rules, auto-response rules, workflow rules, and other customizations that take time to execute)
* before-save updates in flows are executed immediately **prior** to Apex before triggers.

Because of their speed, Salesfrce recommend that you use before-save updates in flows to update fields on new or changed records. 
* You can even avoid the limit for maximum CPU time on the Salesforce servers by replacing Apex code and record-change processes with before-save updates in flows. 

**However, sometimes you need to use a record-change process or an Apex after trigger to:**
* Access field values that are set only after the record is saved, such as the Last Modified Date field or the ID of the new record.
* Create or update related records
* Perform actions other than updating the record that launches the flow e.g. send emails

### How it works
* The $**Record** global variable contains the values from the record that triggers the flow to run. As a result, **there’s no need to add a Get Records element to obtain the record data nor create flow variables to store the record data**
* When the flow changes the values in the $Record global variable, Salesforce automatically applies those new values to the record. So there’s no need to add an Update Records element to save the new values to the database.


## Take a Flow Path Only When Certain Record Changes Are Made
* you can filter out record updates that are unrelated to your flow’s use case
* avoid reprocessing records that previously triggered the flow


* **When you configure a Decision outcome, you can now set that outcome to execute only when the triggering record is updated to meet the condition requirements**

This option gives your flows a powerful filtering feature similar to the ISCHANGED function found in Workflow Rules and Process Builder and the oldMap/newMap variables found in Apex
Build more of your automation directly in Flow Builder without requiring Process Builder or Apex to check the prior version of the data

### How it works
* On a record-triggered flow, configure the Start element to trigger when the record is updated, or when it’s created or updated.
* Only if the record that triggered the flow to run is updated to meet the condition requirements









