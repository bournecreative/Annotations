---
description: installation to get you up and running
---

# Laravel Mix - starter

## Getting started

Getting started is straightforward. The only step I found odd is the last one. After installing, I was wondering why the webpack.mix.js file was not in the root. The last step takes care of this.

[https://laravel-mix.com/docs/4.0/basic-example](https://laravel-mix.com/docs/4.0/basic-example)

```text
cp node_modules/laravel-mix/setup/webpack.mix.js ./
```

### Windows compatibility

Ensure you install "cross-env". 

[https://www.npmjs.com/package/cross-env](https://www.npmjs.com/package/cross-env)

```text
npm install --save-dev cross-env
```

Update the package.json, appending _**cross-env**_ to each script

```text
"watch": "cross-env NODE_ENV=development node_modules/webpack/bin/webpack.js --watch --progress --hide-modules --config=node_modules/laravel-mix/setup/webpack.config.js",
```

Update webpack.mix.js file with 

```text
.setPublicPath("./")
```

