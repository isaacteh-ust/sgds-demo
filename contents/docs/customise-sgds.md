---
title: Customise SGDS with Sass
layout: layout-sidenav
permalink: /docs/customise-sgds/
---
Overview
--------

Use [Sass](https://sass-lang.com/) to customise how SGDS looks and behaves in your project

* * *

### Working with SGDS's source files

#### If you installed sgds with NPM

The Sass source files for sgds can be found under `node_modules/sgds-govtech/sass`:

{%- highlight plaintext -%} site-folder/ ├── scss │ └── custom.scss └── node\_modules/ └── sgds-govtech/sass/ └── sgds.scss {%- endhighlight -%}

#### If you manually downloaded SGDS

If you've manually [downloaded](/docs/getting-started) the Sass files and are not using a package manager, you can set up your code with the following folder structure:

{%- highlight plaintext -%} site-folder/ ├── scss │ └── custom.scss └── sgds/sass/ └── sgds.scss {%- endhighlight -%}

* * *

### Importing and overriding SGDS styles

Import all styles:

{% highlight scss %} // Version 1.0.24 @charset "utf-8"; // Override SGDS defaults $primary: black; $secondary: darkorange; $warning: red; // This must be overridden if you want to use icons! See below for more details $sgds-font-path: "../../../fonts"; // Import all of sgds @import "../node\_modules/sgds-govtech/sgds/sass/sgds.scss"; // If using Webpack @import "~sgds-govtech/sgds/sass/sgds.scss"; {% endhighlight%}

or import individual components as needed:

{% highlight scss %} @charset "utf-8"; $primary: black; $secondary: darkorange; $warning: red; // This must be overridden if you want to use icons! See below for more details $sgds-font-path: "../../../fonts"; // Required sass files @import "../node\_modules/sgds-govtech/sgds/sass/sgds-customise/all"; @import "../node\_modules/sgds-govtech/sgds/sass/sgds-base/all"; // Optional @import "../node\_modules/sgds-govtech/sgds/sass/sgds-components/sgds-masthead"; @import "../node\_modules/sgds-govtech/sgds/sass/sgds-components/sgds-navbar"; @import "../node\_modules/sgds-govtech/sgds/sass/sgds-components/sgds-side-navigation"; @import "../node\_modules/sgds-govtech/sgds/sass/sgds-components/sgds-footer"; @import "../node\_modules/sgds-govtech/sgds/sass/sgds-components/sgds-button"; @import "../node\_modules/sgds-govtech/sgds/sass/sgds-components/sgds-accordion"; // If using Webpack @import "~sgds-govtech/sgds/sass/..."; {% endhighlight%}

#### Overriding `$sgds-font-path` to properly load icons

If you are building a single-page application (such as React or Vue) and use Webpack to compile your Sass files into inline styles (using style-loader), you **must** override the `$sgds-font-path` variable when importing _all styles_ (sgds/sass/sgds.scss) or _sgds-icons_ (sgds/sass/sgds-icons). Otherwise you may encounter a build error stating that the path to the `../fonts` folder cannot be resolved.

#### Explanation

When importing SGDS's Sass, Webpack has to resolve its `fonts` folder relative to the node module's sgds-icons folder in order to load inline styles correctly. This usually means that you would need to point Webpack to the correct fonts folder manually by overriding `$sgds-font-path`. For instance, with the following folder structure:

{% highlight plaintext %} node\_modules/ └── sgds-govtech/ ├── fonts/ │ └── font files └── sgds/ └── sass/ └── sgds-icons/ {% endhighlight %}

The path from `sgds-icons/` to the `fonts/` folder is `../../../fonts`, which would be what `$sgds-font-path` must be set to.

For more information, see the [sass-loader documentation](https://webpack.js.org/loaders/sass-loader/#problems-with-url)

* * *

### The following default SGDS variables can be overridden:

{% for variable\_name in site.data.initial-variables %} {% endfor %}

Variable

Default Value

Type

`{{ variable_name[1].name }}`

{% if variable\_name\[1\].type == 'colour' %} {% endif %} `{{ variable_name[1].value }}`

[{{ variable\_name\[1\].type | capitalize }}](/docs/{{ variable_name[1].type }})