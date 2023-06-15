# Reusable elements

## Naming

**PascalCase** was chosen to be the naming case used for reusable elements since it follows the way components are named in traditional code frameworks, such as ReactJS.

Reusable elements are recommended to be labeled with tags. This will be explained below.

## Classification

Reusable elements (RE's for short) are extremely useful not just for their reusability. Bubble's mechanisms allow RE's to modularize and detach the workflows and logics to a separate view, making it way easier to manage. Hence, RE's can be used for more purposes than just for the sake of reusability. We have broken down the types of RE's as followed:

* **Container**: A big component with self-contained UI, UX and business logic inside. A Container corresponds to an organism in Atomic Design methodology. Sometimes a Container is not reused: it is used only once in a Bubble page, but we split it out to encapsulate the UI, UX and business logic.\
  The name "Container" is still kind of vague, so we have broken it down to several sub-types. If your reusable component doesn't fit those descriptions, you can label it as Container&#x20;
  * **Drawer**: Either a popup or floating group that slide in from the edge of the screen. We use Drawer for popup-ish use cases, where we display a large amount of information.&#x20;
  * **Dialog**: A popup that shows up in the middle of the screen. Dialogs are conversational with the end-user: They answer an action from the user, present them with some inputs, call to actions, etc.&#x20;
  * **Subpage**: This is a "Page" when we want to do single-page behavior. Usually a Subpage has the completeness of a page, but multiple subpages will be added into a Bubble page and toggled conditionally. This allow the end user to switch between contextually different "pages" without the slow delay of Bubble's page change.
* **Workflow**: Invisible components that encapsulate workflows only. Those elements are used to reuse a set of "Custom Events" (Bubble allows you to call for custom events inside a reusable component from the page).&#x20;
* **Component**: This is a small, highly reusable component. For example, in a social network, we have a like button with logics that manage the number of "likes" of a post. This component can be embedded everywhere, from a full post details page, to a shortened post container on the newsfeed. A component corresponds to a Molecule in Atomic Design Methodology.

With this classification, the full name of a RE should be **`[{RE type}] {REName}`** (e.g. **`[Component] LikeButton`**)
