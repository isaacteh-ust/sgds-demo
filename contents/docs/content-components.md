---
title: Documentation
layout: layout-default
permalink: /docs/components 
category: Docs 
breadcrumb: Docs 
published: no 
---

### {{ page.title }} {.has-text-secondary}

-   [Components](/docs/components)
-   [Templates](/docs/templates)

#### **Mandatory** components for all gov.sg websites. {.margin--top .margin--bottom}

{% assign components = site.standard | sort: 'order'%} {%- for component
in components -%}

[]({{%20component.url%20}})

{{ component.title }} {%- if component.js -%} JS {%- endif -%}

{%- endfor -%}

* * * * *

#### Site layout and structure {.margin--top .margin--bottom}

{%- for component in site.layouts -%}

[]({{%20component.url%20}})

{{ component.title }} {%- if component.js -%} JS {%- endif -%}

{%- endfor -%}

* * * * *

#### Plug-and-play components {.margin--top .margin--bottom}

{%- for component in site.general -%}

[]({{%20component.url%20}})

{{ component.title }} {%- if component.js -%} JS {%- endif -%}

{%- endfor -%}

Visit [GUIDES](/guides)for more tips.
