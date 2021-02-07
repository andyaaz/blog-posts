---
title: "Create your first sharable eslint config"
description: "Tired of setting up config file every single time you create a new project?"
slug: "reusable-linter-config"
createdAt: "2020-08-23"
tags: ["how-to", "npm", "eslint"]
---

## Problem

If you have been coding in JavaScript for a while, you might have done something that I always do before writing the first line of actual code - setting up eslint and prettier. It does not take long but sometimes I wish I could use my old configs without having to go back my old repo, copying and pasting. Using it as a npm package might be the perfect solution. Here is how you can use your eslint config as a npm package with some flexibility.

This is even more useful if you work in a team and you want everyone to share the same configurations.

## End Result

```json
// .eslintrc in your new project root

// your npm package is @yourscope/eslint-config
{
  "extends": [
    "@yourscope" // same as @yourscope/eslint-config. eslint is smart enough to figure out the package name
    "@yourscope/eslint-config/react" // only use react specific config
    "@yourscope/eslint-config/gatsby" // only use gatsby specific config
    "@yourscope/eslint-config/<anything>" // <anything> is up to your package structure
  ]
}
```

## Steps

1. Set up your eslint-config repo
2. Publish it to npm
3. Use it in your new project

### 1. Set up your eslint-config repo

1.0 Go npmjs.com to register an account. NPM username will be refered as `my-npm-username`.

1.1 Create a directory and initialize the project

```bash
mkdir eslint-config && cd $_
npm init --scope=@my-npm-username -y
```

1.2 Install eslint and any config or plugin you may need. Let's just install eslint for now.

```bash
npm i eslint
```

1.3 Write your configurations in `eslint-config/index.js`

```js
module.exports = {
  rules: {
    quotes: [2, "single"],
  },
};
```

Now we here ready to publish it to npm.

### 2. Publish it to npm

run

```bash
npm publish --access public
```

### 3. Use it in your new project

Now go to your new project and install the npm package you just published (assuming that package.json exists).

```bash
cd new-project
npm i @my-npm-username/eslint-config
```

```js
// In your .eslintrc
module.exports = {
  extends: ["@my-npm-username"],
};
```

Congrats! Now if you need different configuration for another project, you can always add another file to `@my-npm-username/eslint-config` and export that file then use it with

```js
extends: ['@my-npm-username/eslint-config/some-config']
```

## Read more

[Eslint](https://eslint.org/docs/developer-guide/shareable-configs) has a more comprehensive guide on this if you are interested in a more comprehensive version of this.

Also read more on publishing scoped npm package [here](https://docs.npmjs.com/creating-and-publishing-scoped-public-packages)
