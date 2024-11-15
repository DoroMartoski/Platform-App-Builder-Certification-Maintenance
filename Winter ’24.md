### Build Screen Flows with Reactive Components
Reduce # of screens
Build screens that feel like single page applications with reactive flow screen components.
Configure supported standard components or custom lightning web components to react to changes in other components on the same screen in real time.

For example, create a Data Table component that lists Opportunity records. On the same screen, add a Radio Buttons component, and set the default value of the component to the stage of the first Opportunity that the user selects. 
Previously, if you needed a component to react to changes in another component, you placed the components on separate screens.

How: For screen flows that are configured to run on API version 59.0 and later, you don’t need to take any extra steps to access reactive components.

For screen flows that are configured to run on API versions 57.0 and 58.0, on the Process Automation Settings page, select Enable Reactive Components for Screen Flows running API Version 57.0 and 58.0. Add components to your screen, and save and run your flows as usual.

The Enable Reactive Components for Screen Flows running API Version 57.0 and 58.0 setting expires in Winter ’25. Before that release, upgrade your flows to run on API version 59.0 or later to take advantage of reactive components.

### Build Screen Flows with Reactive Global Variables
Save time by referencing global variables in reactive formulas on flow screens. Use custom labels in reactive formulas to display translatable text to your users. 
For example, create a custom setting called DiscountPercentage, which specifies org, profile, and user discount percentages. 
Reference the variable in reactive formulas across a screen flow. The screen flow applies the correct discount value for the user running the flow and recalculates the value as the user makes changes.  

### Build Screen Flows with Reactive Selections
Use choice components to respond to user selections elsewhere on the same screen. For example, on a flow screen used for returning merchandise, create a Picklist component with reasons for the return such as Don’t Want. 
Then add a Radio Buttons component to automatically select how the customer funds are returned, such as Store Credit.

### Use More Formula Functions in Reactive Screens
If your flows run on API version 59.0 or later, you can now configure a flow screen component to perform real-time logic with the SUBSTITUTE, ADDMONTHS, and ^ formula functions. 
When the flow detects a change to a value referenced in the formula, it immediately recalculates and updates the value of the corresponding screen component. 

### React to Changes on the Same Screen Using Display Text Components
Configure a Display Text component to react to changes in other components on the same screen. 
For example, you have a Currency component, where a user enters the wholesale cost of an item, and a Display Text component that shows the retail price of the item, which is three times the wholesale price. Each time the user updates the wholesale cost, the flow updates the displayed retail price.

### Reactive Components Update the First Time a Screen Loads
A flow now updates the value of a field when the screen loads if the field is configured to react to changes in another field on the same screen. 
If you navigate to a previous or later screen and then return to the current screen, the flow doesn’t update the reactive components again. 
Previously, fields didn’t update unless the user performed an additional action, such as manually changing a value in a field. This change applies only to flows that are running on API version 59.0 or later.

### Inform Screen Reader Users of Reactive Changes on a Flow Screen
Upgrade your flows to run on API version 59.0 or later to let screen reader users know when flow screen components change due to their actions on other components on the same screen. 
For example, if a user changes a field on a screen that results in a component on the screen becoming visible, the screen reader announces, “Due to your recent changes, the content on the screen has changed.”
