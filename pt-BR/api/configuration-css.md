---
title: "API: The css Property"
description: Nuxt.js lets you define the CSS files/modules/libraries you want to set globally (included in every page).
---

# The css Property

> Nuxt.js lets you define the CSS files/modules/libraries you want to set globally (included in every page).

In case you want to use ```sass``` make sure that you have installed ```node-sass``` and ```sass-loader``` packages. If you didn't  just

```sh
npm install --save-dev node-sass sass-loader
```

- Type: `Array`
 - Items: `String`

In `nuxt.config.js`, add the CSS resources:

```js
module.exports = {
  css: [
    // Load a node module directly (here it's a SASS file)
    'bulma',
    // CSS file in the project
    '@/assets/css/main.css',
    // SCSS file in the project
    '@/assets/css/main.scss'
  ]
}
```

Nuxt.js will automatically guess the file type by it's extension and use the appropriate pre-processor loader for webpack. You will still need to install the required loader if you need to use them.