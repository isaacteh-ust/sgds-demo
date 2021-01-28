---
title: Email Address
layout: layout-docs
permalink: /patterns/email-address
redirect_from:
    - /collections/_patterns/email-address
---
Email address input
-------------------

Use this pattern when you need to ask users for their email address.

**Note:** State clearly what their email address will be used for.

* * *

### Usage

Below you will find a **General Email Address** you can use, along with the code needed to build this element.

Email Address Your email would be used for announcements

{%- highlight html -%}

Email Address Your email would be used for announcements

{%- endhighlight -%} Copy snippet

* * *

### Guidelines

#### Explain the rationale of requesting for users’ email address

This allows users to:

*   Feel assured that their email address will not be misappropriated
*   Choose which email address they prefer to use

#### Make sure it works for all users

*   Your field text should accommodate the maximum length of email addresses (256 characters long, including punctuation)

#### Guide users to enter their email address

Make it easier for users by:

*   Allowing them to copy and paste their email address
*   Setting the `type` attribute to `email` so that the correct keyboard is displayed
*   Setting the `spellcheck` attribute to `false` so that their email addresses are not spell checked by the browser or device
*   Setting the `autocomplete` attribute so that browsers can fill in their email address if they have entered it previously
*   You will need to include the `autocomplete` attribute to meet [WCAG 2.1 AA](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html) for production.

* * *

{%- include sgds-feedback.html -%}
