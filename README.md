# babel-plugin-dev-debug

an babel plugin that for dev debug

## why

Sometimes we need to write some logic in the development environment for debugging and development purposes

However, we don't want the debug code to be released to the production environment

This plugin is designed to solve this problem

## Install

```shell
npm i babel-plugin-dev-debug
```

## Usage

1. add babel-plugin-dev-debug plugin to babel.config.js

```js
// babel.config.js
module.exports = {
  plugins: ["dev-debug"],
};
```

2. in you code

```js
if (DEBUG) {
  // for debug
  // must be removed in production env
  const a = 10;
  const b = 20;
  console.log(a + b);
}
```

if you use eslint you must be add DEBUG to globals to eslint.config.js

```js
// .eslintrc.js
module.exports = {
  globals: {
    DEBUG: true,
  },
};
```
