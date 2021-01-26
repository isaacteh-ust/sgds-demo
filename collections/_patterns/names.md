---
title: Names
layout: layout-docs
---
{% capture general\_name\_field %}

Full Name

{% endcapture %} {% capture multiple\_name\_field %}

Given Name

Family Name

{% endcapture %}

Collecting names
----------------

Use this pattern when you need to ask users for their names.

* * *

### Types

#### 1) General name field

You should follow this pattern when you need to ask for a user’s name. You should only ask for names if you need it for a service.

{{general\_name\_field}}

{%- highlight html -%}{{general\_name\_field}}{%- endhighlight -%} Copy snippet

* * *

#### 2) Multiline name field

You should follow this pattern when you know that your users will follow the given-name and family-name convention.

{{multiple\_name\_field}}

{%- highlight html -%}{{multiple\_name\_field}}{%- endhighlight -%} Copy snippet

* * *

### Guidelines

#### Make sure the name field works for your users

*   Name fields should be long enough to accommodate the names of your users
*   Make sure that you support all characters that users may need to enter, including symbols and numbers
*   Set the `spellcheck` attribute to `false` so that you do not spellcheck a user's name

#### Single name fields

*   This accommodates the widest range of name types and formats
*   Reduces the risk of users entering their name in the incorrect format
*   However, by using this, you may not be able to extract parts of a name

#### Multiple name fields

*   Use multiple name fields with discretion. Not everyone's name fits the general first-name, last-name convention.
*   Using multiple name fields increases the risk of a person's name not fitting the same convention. Hence, it may be entered incorrectly.

#### Labelling of name fields

1\. For **single name** fields, use "Full Name".

2\. For **multiple name** fields, use:

*   'Given Name'
*   'Family Name'

Make it clear whether you are asking for a user's common name, or as written on an official document such as NRIC or passport.

If you are unsure of how your users will fill in their name or know that you have a wide range of users with different formats for their names, it is highly recommended to use a single name field to prevent errors and confusion.

This is to ensure that your users:

*   Do not get confused as to how they should be filling in their name
*   Reduce the risk that their name may be filled in wrongly

#### Autocomplete

Use the `autocomplete` attribute when asking for a user's name. This makes it easier for the user to fill in their name if they have done so previously on the browser.

*   Full name: use `name`
*   Given name: use `given-name`
*   Family name: use `family-name`

You will need to include the `autocomplete` attribute to meet [WCAG 2.1 AA](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html) for production.

* * *

{%- include sgds-feedback.html -%}
