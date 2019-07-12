---
description: installation to get you up and running
---

# Laravel Mix - boilerplate

## **Starting a project in Laravel**

{% embed url="https://laravel-mix.com/docs/4.0/installation" %}

* npm init
* install Laravel as dev dependency
* copy webpack.mix.js file to root

```text
cp node_modules/laravel-mix/setup/webpack.mix.js ./
```

### **Update webpack.mix.js file**

* update source and destination paths for js and css files
* setPublicPath
* Update package.json scripts.

```text
// this is required for Windows
npm install cross-env --save-dev
```

Create file tree as defined in webpack.mix.js. Add scss, js and index.html

**Npm run dev to get Laravel to install initial dependencies. Run again to build dist files. Be patient.**

### **Update webpack.mix.js file**

Find browserSync and add the following key value pairs

```text
proxy: ‘http://localhost:8080/
files: [“src/**/*.*”, “*.html” ]
```

**Npm run hot to get Laravel to install dependencies for browserSync Run again to build dist files. Be patient.**

Install slick-carousel as a dev dependency

```text
--save-dev slick-carousel
```

Install jquery as a dev dependency

```text
--save-dev jquery
```

Install @vzrf/core as dependency

```text
--save @vzrf/core
```

### **Update webpack.mix.js file**

Add auto loading for jquery just as specified here:

{% embed url="https://laravel-mix.com/docs/4.0/autoloading" %}

Incorporate code splitting to separate vendor libraries into their own files

{% embed url="https://laravel-mix.com/docs/4.0/extract" %}

```text
mix.extract(['vue', 'jquery']);
```

### **Update index.html to reflect destinations for compiled css and js**

```text
// link to your stylesheets
href = “dist/css/app.css”
 
// link to your js files. Also ensure correct order if code splitting is leveraged.
<script src="/js/manifest.js"></script>
<script src="/js/vendor.js"></script>
<script src="/js/app.js"></script>
```

