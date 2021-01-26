---
title: Installation
layout: layout-sidenav
permalink: /docs/installation/
---
Installing SGDS
---------------

* * *

### Install directly in browsers using a free and highly available CDN:

#### CSS

{% highlight html %} ...    ... {% endhighlight %}

#### JavaScript

[Certain components](/docs/) of SGDS make use of JavaScript, with jQuery as an external dependency. **If you only need the visual parts of SGDS (i.e. css), you do not need to import the following.**

{% highlight html %} ... ... {% endhighlight %}

* * *

### Install using npm

Frontend developers can use npm to download sgds and use it as a dependency in their projects. Using npm is especially useful when using a module bundler or build tool, such as [Webpack](https://webpack.js.org).

*   Install [Node.js](https://nodejs.org/en/download/), which includes an installation of npm.
*   Install sgds by navigating to your site's codebase folder using your terminal and run: `npm install sgds-govtech`
*   This will download sgds into `node_modules/sgds-govtech` in your current folder: {%- highlight bash -%} site/node\_modules/sgds-govtech/ ├── css/ ├── fonts/ ├── js/ ├── \* sgds/sass/ {%- endhighlight -%} _\* SGDS Sass source files, for [advanced usage](/docs/customise-sgds)._
*   If you use a module bundler like Webpack, import sgds in your entry point: {% highlight javascript %} import "sgds-govtech/css/sgds.css"; import "sgds-govtech/js/sgds"; // Do not use with other web frameworks! {% endhighlight %} _\*Note that usage with frameworks such as React, Vue or Angular is discouraged since they manipulate the DOM in their own environments. Framework-specific implementations are in early development and can be found at [sgds-govtech-react](https://github.com/govtechsg/sgds-govtech-react) and [sgds-govtech-vue](https://github.com/govtechsg/sgds-govtech-vue) ._

* * *

### Install manually

You can download minified sgds CSS and JavaScript files and host them yourself in your production environment.

[Download SGDS package](/assets/downloads/sgds-govtech.zip)

The zip package contains the following files:

`css/sgds.css`

`js/sgds.js`

`fonts/sgds-icons.svg`

`fonts/sgds-icons.wott`

`fonts/sgds-icons.ttf`

`sgds/sass/...`(source files for [advanced usage](/docs/customise-sgds))

*   Extract and copy the files and folders into a relevant place in your project’s code base
*   Reference the CSS and JavaScript files in each HTML page or templates in your project, same as above. Note that [certain components](/docs/) of SGDS make use of JavaScript, with jQuery as an external dependency. {%- highlight html -%} ...  ...    {%- endhighlight -%}

* * *

### Open source

The SGDS source is written in Sass and JavaScript. Usage and development instructions can be found at [https://github.com/govtechsg/sgds](https://github.com/govtechsg/sgds). Bug reports and pull requests are also [welcome!](https://github.com/govtechsg/sgds/issues)

* * *

### Content Management Systems

*   Sitefinity
*   Wordpress

#### Install Sitefinity Resource Package

The **Sitefinity resource package** is in the pilot phase, your valuable [feedback]({{ site.feedback_form }}) will help us in improving it.

 [Download Sitefinity resource package](/assets/downloads/sgds-sitefinity-theme.zip)

All you have to do is copy the **Sitefinity resource package** folder and paste into your `ProjectName / ResourcePackage` folder and rebuild the project.

The Sitefinity **DesignSystem** resource package consist of:

1.  SGDS Stylesheet  
    `/DesignSystem/assets/dist/css/sgds.css`
2.  SGDS Javascript  
    `/DesignSystem/assets/dist/js/sgds.js`
3.  SGDS Icon Library  
    `/DesignSystem/assets/dist/fonts/`
4.  SGDS Grid System Template  
    `/DesignSystem/GridSystem/Templates`
    *   Section template  
        `sgds-section.html`
    *   Container template  
        `sgds-container.html`
    *   Grid Columns  
        `sgds-grid-x.html`
5.  Master layout with the DSS compliant Mandatory components  
    `/DesignSystem/MVC/Views/Layouts`
    *   Gov.sg masthead
    *   Navigation bar widget  
        `/DesignSystem/MVC/Views/Navigation/NavigationView.sgds.cshtml`
    *   Footer

#### Install Wordpress

The **Wordpress theme** is in the pilot phase, your valuable [feedback]({{ site.feedback_form }}) will help us in improving it.

 [Download Wordpress Theme](/assets/downloads/sgds-wordpress-theme.zip)

Adding the Wordpress theme to your project:

1.  Log in to the WordPress Administration Panels.
2.  Select the Appearance panel, then Themes.
3.  Use the Upload link in the top links row to upload the Wordpress theme that you have previously downloaded to your machine.
4.  To activate the Theme click the Activate button.