---
description: Notation of state, data, clickable and elements grouping
---

# Other notations

## Notation of state, data & clickable

We figured out that elements with custom states, data source or clickability usually required a lot of attention. Without notations, you would need to memorize the elements or painfully search for them in workflows or the element tree. Hence, we recommend adding notations in front of the elements names:

* **\<S>** or **\<State>** for elements with custom states.
* **\<D>** or **\<Data>** for elements with custom data sources (parent elements only, no need to mark child elements that inherit the data).
* **\<C>** or **\<Click>** for non-input elements that are clickable (e.g. texts, groups).

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>An example of using notations</p></figcaption></figure>

This is very efficient while using Bubble's search function, as the < and > differentiate the elements from other elements.

In the case of having multiple notations, you can order the notations however you like, alphabetically for instance. It would be preferable to use shorten forms of the notations though.

## Elements grouping&#x20;

The meaning of _grouping_ here transcends the traditional meaning of nested groups and elements. Instead, please understand this _grouping_ as an umbrella term for element nesting, element classification and categorization according to usage, placement, etc.

In this case, the use of a **\[Tag]** in front of the elements is recommended.&#x20;

An example of this is the case of having 2 identical groups of elements with close usage, yet for a reason you cannot merge them into one. Having tags helps differentiate an element from its identical counterpart in the other group, as well as to perform search for elements better.

Below is an example of 2 forms with identical elements but used for different purposes.

| \[Onboard] Group Form    | \[Invite] Group Form    |
| ------------------------ | ----------------------- |
| \[Onboard] Text Title    | \[Invite] Text Title    |
| \[Onboard] Input Name    | \[Invite] Input Name    |
| \[Onboard] Button Submit | \[Invite] Button Submit |

## Notation of order

Groups, data fields, option set fields, etc when related to ordering (e.g. steps in an onboarding process, indicated by an option set) should come with a number indicator (`no_`) before the name.

Example: 1\_onboardingStep; 2\_onboardingStep

The number should always come before the name to help with sorting.
