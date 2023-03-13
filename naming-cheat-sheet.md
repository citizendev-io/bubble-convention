---
description: For quick reviews during development.
---

# Naming Cheat Sheet

The naming conventions pages below are lengthy, as they not only introduce the naming systems but also explain the thought process behind them. Thus, we want to condense everything here so you can review afterwards. If you happen to make a beautifully visualized and decorated 1-page cheat sheet of this, we are more than happy to attach it here.

## Page naming

Regular/customer facing pages: **kebab-case**

System/non-public pages: **snake\_case**

## Element naming

### Groups

* Structural groups: Use **Header, Body, Footer, Nav, Section, Container** for the corresponding groups.
* Regular groups: Use **`{Group type} {Group name}`** like usual. For example: _Group Testimonials, FloatingGroup Sidebar, Popup Deletion Confirmation._
* Sub groups: Use **`[{Parent's name}] {Group type} {Group name}`**. For instance:
  * Parent group: _FloatingGroup Nav_
  * Sub groups: _\[Nav] Group Menu_
* RepeatingGroups: Use **`RepeatingGroup {Data type}` ** or **`RG {Data type}`**. For instance: _RG Comment_.

### Reusable elements

Reusable elements should be named like pages, with type: **`[{Reusable type}] {reusable element name}`**. For example: _\[Drawer] user-details_

Common reusable types include:

* Container: A big component that contains a lot of elements and logics inside, similar to an _organism_ in atomic design, mainly used for breaking the apps into smaller parts.
* Drawer: Either a popup or floating group that displays data as a drawer, and is also a container.
* Dialog: A popup that is also a container.
* Subpage: For groups used in single-page behavior
* Workflow: Invisible components that encapsulate workflows only.
* Component: Small components, like a simple like button with logics that manage the number of likes.

### Visual elements

* Non-dynamic elements: You should keep the element type first, and then its name, like usual: **`{Element type} {Name}`**. For instance: _Button Submit Feedback._
* Dynamic elements: Use **`{Element type} {Data field}`** or **`{Element type} {Operations}`**. For instance: _Text username_ or _Text firstName + lastName._

### Input elements

Input elements should reflect the data they are changing: ** `{Element type} {Data field}`** or **`{Element type} {Data type/Data field}`**. For instance: _Input username_ or _Input User/username._

### Custom states

To differentiate from data field, use **snake\_case** for custom states. Other than that, custom states should be similar to a data field's name.

### **Notation of state, data & clickable**

* **`<S>` ** or ** `<State>`** for elements with custom states.
* **`<D>` ** or ** `<Data>`** for elements with custom data sources (parent elements only, no need to mark child elements that inherit the data).
* **`<C>` ** or ** `<Click>`** for non-input elements that are clickable (e.g. texts, groups).

Example: _\<S> Group Users_&#x20;

### Notation of order

Groups, data fields, option set fields, etc when related to ordering (e.g. steps in an onboarding process, indicated by an option set) should come with a number indicator (`no_`) before the name.

Example: 1\_onboardingStep; 2\_onboardingStep

## Workflow naming & organization

Workflow naming:&#x20;

* Front-end workflows: Keep as default for simple/general workflows. If workflows are more complicated:
  * Navigating/Screen transition workflows: `Page 1 -> Page 2`.
  * Others: Purpose of the workflow, in **snake\_case**. For instance: _register\_user_ .
* Custom workflows, triggers and API workflows: **snake\_case**.

Color coding is preferable than foldering due to the ease of view. Workflows interacting with the same object (e.g. CRUD operations of User) should be in one color. Workflows with the same purpose (e.g. triggers used for analytics) should be in one folder. Workflow names with **\[Tag]** is also a good approach, as Bubble sorts the workflows by name.

## Database naming

For data types: **PascalCase**

For data fields: **camelCase**&#x20;

For option sets: **SCREAMING\_SNAKE\_CASE**&#x20;

For option set fields:

* Use regular texts when the field needs to be displayed to end-users.
* Use rules like data fields for regular fields.
* Use **kebab-case** if the `Display` field is used for URL param.
