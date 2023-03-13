# Option sets

## Classification of option sets

Option sets are extremely useful and we want to have this special section to talk about how we usually harness their power. They can be used as and broken down into 3 types:

> Please keep in mind that at the core, Bubble handles option sets differently from data types, however they are represented similarly in terms of structure.

* Enumerated types: This is the most common use of option sets as they are used to store static data. For instance, an option set can store different values of user roles (e.g. admin, employee, analyst).&#x20;
* System configurations: In the case of having parameters that you want to use across the application, it is recommended to you option sets to save those and reuse in workflows and elements so that if you need to alter them, you wouldn't need to get to each and every workflow and element to change the values. An example of this is having some kind of limit, like seat limit for SaaS apps, that you want to alter later on after some pivoting.&#x20;
* Navigation and control: In case of navigation, either single-page or multi-page, using states or URL params, it is recommended to use option sets to store pages and sub-pages names as well. Plain text is not recommended when it comes to URL params as it is more difficult to maintain.

> In fact app texts are also very useful when it comes to system configurations, however app texts are, obviously, limited to texts.&#x20;
>
> Please keep in mind that sensitive information should not be stored in option sets.

## Option set naming

Since option sets are used as system configurations, we learnt from traditional programming and chose **SCREAMING\_SNAKE\_CASE** for option sets' names. This helps differentiate them from regular data types.

For fields inside option sets, the built-in _Display_ field is usually literally used for display, so we would recommend using regular text that is suitable for display for this (e.g Admin, Employee, Analyst). If there are fields not used for display, you can simply follow [Data types & fields](data-types-and-fields.md)'s instructions.

When an option set is used for managing navigations in a single-page behavior, it is recommended to use **kebab-case** for the _Display_ field. When the option is displayed on the URL for instance, it will look like a page name.
