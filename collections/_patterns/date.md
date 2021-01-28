---
title: Date
layout: layout-docs
permalink: /patterns/date
redirect_from:
    - /collections/_patterns/date
---
Date input
----------

Use this pattern when you want to ask users for a specific date, e.g their date of birth or when something was issued to them.

**Note:** If you need users to select from a few specific dates, we recommend that you use the radio button component to allow them to choose easily.

* * *

### Usage

Below you will find a **General Date Format** you can use, along with the code needed to build this element.

{% capture date %}

Please enter your date of birth E.g 01 01 1990

Day

Month

Year

{% endcapture %}

{{date}}

{%- highlight html -%}{{date}}{%- endhighlight -%} Copy snippet

* * *

### Guidelines

#### When you require users to fill in dates for your services

*   State clearly how the data should be filled (e.g. **Day Month Year**)
*   Give an example of how the date should be filled in (e.g. **01 01 2020** vs **1 1 2020**)

#### When you request users to fill in memorable dates

*   For example, asking for Date-Of-Birth means you should always have the `autocomplete` attribute for these 3 fields, `bday-day`, `bday-month` and `bday-year` to bring convenience to users.
*   You will need to include the `autocomplete` attribute to meet [WCAG 2.1 AA](https://www.w3.org/WAI/WCAG21/Understanding/identify-input-purpose.html) for production.

* * *

{%- include sgds-feedback.html -%}