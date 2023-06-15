# Custom states

## Naming

To differentiate custom states from data fields and data types, use **snake\_case** for custom states.

## Placement of states

States can be divided into 2 types:

* **Global states**: States that are accessed and used throughout the whole page, or the whole reusable element.
* **Local states**: States that are used only within a group or an element.

Generally, **global states** should obviously be placed in the global element (in a page or in a reusable element). Since states are placed there by default, there is no need to additionally label the page/reusable element.&#x20;

However, placing states in a reusable element exposes the states to other elements in the page to access (not a bug but a feature!). So, if you want to truely encapsulate a reusable element and only expose controllable states to the page, consider placing the other states in the Body or main container of the reusable element.  &#x20;

**Local states** should also be placed in the global element they are not numerous for the ease of access. They should only be placed locally (in the group that wraps the elements that uses those states, or the atomic elements themselves) if they are numerous. In that case, Element naming/Other notation page talks a bit about naming elements that have custom states in them.
