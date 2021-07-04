##Objectives:

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

###Debug flow errors in a sandbox org as another user

* Process Automation Settings --> select the Let admins debug flows as other users checkbox
* open a flow in Flow Builder and click Debug
* Select the Run flow as another user checkbox, and choose a user to impersonate.

**Debugging a flow as another user is available only for screen flows and autolaunched flows in nonproduction orgs**
**Any operations performed by screen components are performed as the logged-in user and not as the impersonated user.**