---
title: Getting Started
layout: layout-sidenav
permalink: /docs/getting-started/
redirect_from:
    - /docs/
    - /contents/docs/getting-started
---
Overview
--------

[Installation](/docs/installation)

[Advanced customisation with Sass](/docs/customise-sgds)

We highly recommend that you customise your site, by extending base SGDS classes using separate CSS or [Sass](/docs/customise-sgds) files.

This way, your site will automatically inherit non-conflicting fixes and improvements made to SGDS without breaking existing styles.

Here are the items you’ll need:

*   [Installation of SGDS](/docs/installation).
*   [Use advanced customisation with Sass](/docs/customise-sgds).

**Note:** Links that contain the JS tags contain interactive elements that require [JavaScript](/docs/installation).

If you are using a JavaScript framework, check out the framework-specific helper libraries:

*   [React](https://github.com/govtechsg/sgds-govtech-react)
*   [Vue](https://github.com/govtechsg/sgds-govtech-vue)

* * *

### Component reference

Component reference is helpful for you to implement layouts, elements and components, using our CSS class and modifiers.

Each page provides you with comprehensive usage instructions, examples and guidelines.

* * *

### Standard Components

Standard components aid users in basic site identification and navigation. They should be present in all **.gov.sg** websites as stated in the [Digital Service Standards](https://www.tech.gov.sg/digital-service-standards/).

{% include component-list.html collectionName='standard' %}

* * *

### Layout

CSS classes are used for composing your site layout. Over here, you can also find the breakpoints that we use for desktop and mobile devices.

{% include component-list.html collectionName='layout' %}

* * *

### General

Common components that can be used individually or grouped to form patterns and templates. For example, you can group the hero with cards to build a landing page.

{% include component-list.html collectionName='general' %}

* * *

### Form

Form components and guidelines for the collection of user input.

{% include component-list.html collectionName='form' %}

* * *

### Helpers

Helper classes to help you alter the style of almost any component.

{% include component-list.html collectionName='helpers' %}
