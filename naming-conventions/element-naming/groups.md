# Groups

Groups make up the structure of an application, hence a dedicated page to explain the naming of groups (because, you know, they are supposed to be in the Visual elements page).&#x20;

Group names are recommended as followed.

### Structural groups

Structural groups are the most outer groups within a page. They define the structure of a page.

Structural groups are recommended to use the following names and categorization. These names are inspired by HTML tags as well as component names from other visual builders such as WordPress Oxygen Builder or Webflow.

* **Header**: For the header, obviously. If it's a reusable component, either **`Header`** or **`[Container] Header`** should be fine.&#x20;
* **Footer**: Similar to Header.
* **Body**: The main container of the page. This should be used to control max width or padding of the page's inner content, so it's a very important group. Many modern layouts are not full width (e.g. Facebook), so using a Body group helps maintain the width of the contents. A basic layout of a page consists of a Header, a Body and a Footer.&#x20;
* **Section**: In the case of multiple sections with different widths required, the Body can be broken down into multiple smaller sections.

### Regular groups

It's highly recommended that the Group type (e.g. Popup, FloatingGroup) should persist being in front of the name like usual:  **`{Group type} {Group name}`**. This is for Bubble to sort the elements by type, and for users to easily recognize the type of the element. Swapping the type and the name makes more sense grammatically, but not programmatically. For example: **`Group Testimonials`**_,_ **`FloatingGroup Sidebar`**_,_ **`Popup Deletion Confirmation`**_._

> It's similar to a thing in traditional code called _type declaration_.

### Sub groups

Occasionally, the groups in a page require a way to be grouped together in other for the ease of management, without having to break them into a separate reusable element. This is similar to the grouping demonstrated in the Other notations page.&#x20;

In that case, you can use **`[{Parent's name}] {Group type} {Group name}`**. For instance:

* Parent group: **`FloatingGroup Nav`**
* Sub group: **`[Nav] Group Menu`**

### Repeating groups

Repeating groups have to come with a data type. Hence, the data type is recommended to be referred to directly in the name: **`RepeatingGroup {Data type}`** or **`RG {Data type}`**. For instance: **`RG Comment`**.

