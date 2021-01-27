---
title: Address
layout: layout-docs
permalink: /patterns/address/
---
Collecting addresses
--------------------

Use this pattern when you require users to key in their Singapore-based address.

**Note:** Give your users the option to either key in their postal code to look up their address, or enter their full address manually.

* * *

### Usage

Below you will find a **General Address Format** you can use, along with the code needed to build this element.

{% capture address %}

Postal Code

Find Address

Block/Street Name

Building/House Number If applicable

Unit Number

{% endcapture %}

{{address}}

{%- highlight html -%}{{address}}{%- endhighlight -%} Copy snippet

* * *

### Guidelines

#### For your Address Lookup

*   Make it clear to users that this will only work with Singapore addresses.
*   Use the address lookup **only** if you are asking for a **Singapore address**. Otherwise, use multiple text inputs or a text area when asking for addresses outside of Singapore.

#### For Manually-entered Addresses

*   The fields should always have the `autocomplete` attribute to help your users complete it quickly.
*   You will need to include the `autocomplete` attribute to meet [WCAG 2.1 AA](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html) for production.

* * *

{%- include sgds-feedback.html -%}
