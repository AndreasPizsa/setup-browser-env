# `browser-env-register`

> Simplified browser testing in your node test suite.

# Motivation

`browser-env-register` lets you register a simulated browser environment using [browser-env], saving the hassle of creating and loading a test-helper file.

# Features

+ ✅ **Compatible.** Works with [ava], [mocha] and everything else.
+ ✅ **Configurable.** via `package.json` or `browser-env.{js, json, yaml}`
+ ✅ **Reliable.** 100% Code Coverage.
+ ✅ **Free.** MIT License.

# Usage

## Install

```sh
npm add -D browser-env-register
```

### ava

```js
// package.json

{
  "ava": {
    require: [
      "browser-env-register"
    ]
  }
}
```

### mocha

```js
# mocha.opts
--require browser-env-register
```

## Configuration (optional)

`browser-env-register` runs out of the box without further configuration, but you can set options if needed in your `package.json` or a  `browser-env.{js,json,yaml}` config file.

#### package.json

```
{
  "browser-env": {
    "globals": ['window', 'document'],
    "jsdom": {
      userAgent: 'My User Agent'
    }
  }
}
```


#### Shortcuts

Pass only the of name global properties without setting jsdom options:

```
{
  "browser-env": "window document"
}
```

```
{
  "browser-env": ["window", "document"]
}
```

Pass only jsdom options without setting the of name global properties:

```
{
  "browser-env": {
    "userAgent": "My User Agent"
  }
}
```

[ava]: https://github.com/avajs/ava
[mocha]: https://mochajs.org
[browser-env]: https://www.npmjs.com/package/browser-env
