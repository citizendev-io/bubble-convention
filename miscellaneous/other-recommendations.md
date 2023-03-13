---
description: Recommendations that we don't know where to put
---

# Other recommendations

### Placement of _invisible_ _elements_

_Invisible elements_ comes in handy when you only want to use the logics or JS code that comes with the element. Such an element can be some custom code that comes from a plugin, which is a very common case.

When using such, we'd recommend placing the invisible element either on the page level, far down below the page (before/inside footer) or nearest to the element is affecting (e.g. put the fuzzy search element next to the real search element).

### Project documentation practices

We'll probably have a separate page or even a separate project addressing this since documentation is crucial for development. However, here we have some recommended documents and tools that you can use:

* Use case diagram: A very basic diagram that helps you grasp the actors in a system and the interactions between those actors. This can be achieved with either **FigJam** or **diagrams.net**.
* User stories: A framework that helps you with recording the features on a high level, from the perspective of users. This can be made with **FigJam**.
* Entity Relationship Diagram (ERD): An extremely handy UML (Universal Modeling Language) that is familiar to tech guys. This helps you visualize your database. An ERD can be built using **dbdiagram.io**.&#x20;
* Business Process Modeling and Notation (BPMN): A familiar modeling language used by Business Analysts to document complex procedures. This is extremely useful if your applications contain difficult workflows or user flows. You can create a BPMN with **bpmn.io**.

Disclaimer: We're not taking any money from those providers listed above for promotion. We just see them as the best tools in our opinions to get the work done.

### Single page display/hidden elements

There is one thing with hidding and displaying elements with conditions that is when you set an element to be displayed on load, and then hidden on a certain condition, occasionally the element will display first and then hide when the condition is processed. This creates a glitchy experience for the end users.

With that said, it's UX-wise recommended to have the dynamic elements hidden by default, and then display when a condition is met.

This is better for user experience, yet it comes with a few drawbacks:

* Worse developer experience: The elements won't be displayed so you'll need to navigate the elements tree for the elements.
* Unusable logics or custom code related to a hidden element: Bubble changed the build pipeline a while ago, such that hidden elements won't be loaded onto the front-end if hidden by default so that it saves the rendering capacity and enhance loading speed. Nevertheless, without the elements being loaded, their workflows and code might not be accessible in case you want to use a hidden popup to store some logics.

One other related thing we had figured out during the development of single page applications is the display of floating groups are not controllable by URL parameters. You must use states to show/hide the floating groups. This is discussed more in **Usage recommendations/Layout/Single-page behaviors**.

