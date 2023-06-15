# Data types & fields

## Data type

**PascalCase** should be used for data types.&#x20;

Why? We saw that Bubble used a lot of natural languages in its builder. That is easy to understand, as the tool is aimed at citizen developers. The use of words without spaces helps differentiate the data types from native types and other phrases that Bubble uses.

Why not snake\_case like in regular databases? Bubble automatically capitalizes the first character of the data type in the builder, and Snake\_case looks weird.

**Some notices on choosing names:**

As data types represent "things", their names should be nouns or compounds of nouns. They should be singular as well, as a data type represents the blueprint of 1 singular thing. Bubble also adds _s_'es to the end of the types when you are retrieving a list of them, so a type of _Cars_ would become _Carss_ and that's just weird, unless you try to make it badass.

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption><p>An example of using CamelCase for data types</p></figcaption></figure>

## Data field

**camelCase** should be used for data types.

This is a common presentation used for variables in regular programming, so we thought a resemblance would be good for developers to work with. Moreover, it looks similar to data type's PascalCase, implying their relationship.

**Some notices on choosing names:**

Data fields vary in forms and usage. The approaches for each type are as followed:

* Text, file, image, date, address types: These types can be represented by nouns (e.g. username, homeAddress). If the field is a list of objects, you should use the noun's plural form.
* Number: You should add a word indicating that the field is a number field to help differentiate it from the others. For instance, a field counting the number of cars can be _noOfCars_ or _carsCount._
* Yes/no (aka boolean): We took this one from the best practice in pro-code. It is recommended to use auxiliary verbs to indicate the dichotomy of the attribute. For example, if a blog post can either be private or public, you can use either _isPrivate_ or _isPublic_ to indicate the privacy_._ This is not a perfect approach as you will see Bubble's builder refering to the field as _This Post's isPrivate_, which is not grammarly correct, yet it is easier to understand the purpose of the field.
* Relationship (a field that refers to another data type): We have 2 recommended approaches for this type of field. You can either use nouns like usual, or you can use verbs to indicate the relationships between the 2 data types. For example, for a nested comments structure, you can refer to the parent comment as _parentComment_, or _repliesTo,_ as this comment replies to its parent comment.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>An example of naming data fields</p></figcaption></figure>

## Other recommendations

Sometimes we have fields and types that are used for management on the system level and are not visible to the users and should not be manipulated by the users whatsoever, as they are critical and sentitive. We would not want other developers to mess up those fields as well, hence the need of differentiation. An example of this is the case of multi-tenancy, as you may have fields to control privacy.&#x20;

In this case, it is recommended to add an underscore ( \_ ) in front of the types and fields. This pattern is widely seen in traditional coding as well.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>An example of data types used for system tracking</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption><p>An example of using a field for multi-tenancy (contacts are scoped inside companies)</p></figcaption></figure>

> Airdev (a well known Bubble delivery vendor) usually uses Unicode icons (aka characters, aka emojis) like ⚙️ instead of using underscore. This is not a bad approach at all and it is way better than underscore in terms of visibility, however typing \_ is quicker than having to input such an icon. You can feel free to explore and use the method you prefer.

Sometimes you might have fields or types attached to different actors in your application that you would want to differentiate. In this case, having a \[Tag] in front of the fields or types would help.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption><p>An example of using tags</p></figcaption></figure>

