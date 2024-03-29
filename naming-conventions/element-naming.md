# Element naming

Element naming is the hardest when it comes to standardization for Bubble development. In this document, we covers not just recommendations for element naming but also element types break-down. These types come from creative ways that Bubble developers use the elements to their fullest to demonstrate complex behaviors.

## TL,DR:

### Groups

* Structural groups: Use **Header, Body, Footer, Section** for the corresponding groups.
* Regular groups: Use **`{Group type} {Group name}`** like usual. For example: _Group Testimonials, FloatingGroup Sidebar, Popup Deletion Confirmation._
* Sub groups: Use **`[{Parent's name}] {Group type} {Group name}`**. For instance:
  * Parent group: **`FloatingGroup Nav`**
  * Sub group: _**`[Nav] Group Menu`**_
* RepeatingGroups: Use **`RepeatingGroup {Data type}`** or **`RG {Data type}`**. For instance: **`RG Comment`**.

### Reusable elements

Reusable elements should be named like pages, with type: **`[{Reusable type}] {ReusableElementName}`**. For example: **`[Drawer] UserDetails`**

Common reusable types include:

* Container: A big component that contains a lot of elements and logics inside, similar to an _organism_ in atomic design, mainly used for breaking the apps into smaller parts.
  * Drawer: Either a popup or floating group that displays data as a drawer.
  * Dialog: A popup with CTAs.
  * Subpage: For groups used in single-page behavior.
* Workflow: Invisible components that encapsulate workflows only.
* Component: Small components, like a simple like button with logics that manage the number of likes.

### Visual elements

* Non-dynamic elements: You should keep the element type first, and then its name, like usual: **`{Element type} {Name}`**. For instance: _Button Submit Feedback._
* Dynamic elements: Use **`{Element type} {Data field}`** or **`{Element type} {Operations}`**. For instance: **`Text username`** or **`Text firstName + lastName`**_._

### Input elements

Input elements should reflect the data they are changing: **`{Element type} {Data field}`** or **`{Element type} {Data type/Data field}`**. For instance: **`Input username`** or **`Input User/username`**_._

### Custom states

To differentiate from data field, use **snake\_case** for custom states. Other than that, custom states should be similar to a data field's name.

### **Notation of state, data & clickable**

* **`<S>`** or **`<State>`** for elements with custom states.
* **`<D>`** or **`<Data>`** for elements with custom data sources (parent elements only, no need to mark child elements that inherit the data).
* **`<C>`** or **`<Click>`** for non-input elements that are clickable (e.g. texts, groups).

Example: **`<S> Group Users`**&#x20;

### Notation of element grouping

**`[Tag]`** should be used to group elements together.

### Notation of order

Groups, data fields, option set fields, etc when related to ordering (e.g. steps in an onboarding process, indicated by an option set) should come with a number indicator (`no_`) before the name.

Example: `1_onboardingStep`; `2_onboardingStep`

For further analysis, explanations and examples, please check the below documents out.

{% content-ref url="element-naming/groups.md" %}
[groups.md](element-naming/groups.md)
{% endcontent-ref %}

{% content-ref url="element-naming/reusable-elements.md" %}
[reusable-elements.md](element-naming/reusable-elements.md)
{% endcontent-ref %}

{% content-ref url="element-naming/visual-elements.md" %}
[visual-elements.md](element-naming/visual-elements.md)
{% endcontent-ref %}

{% content-ref url="element-naming/input-elements.md" %}
[input-elements.md](element-naming/input-elements.md)
{% endcontent-ref %}

{% content-ref url="element-naming/custom-states.md" %}
[custom-states.md](element-naming/custom-states.md)
{% endcontent-ref %}

{% content-ref url="element-naming/other-notations.md" %}
[other-notations.md](element-naming/other-notations.md)
{% endcontent-ref %}
