---
id: version-6.26.3-babel-plugin-transform-async-to-generator
title: babel-plugin-transform-async-to-generator
sidebar_label: transform-async-to-generator
original_id: babel-plugin-transform-async-to-generator
---

## Example

**In**

```javascript
async function foo() {
  await bar();
}
```

**Out**

```javascript
var _asyncToGenerator = function (fn) {
  ...
};
var foo = _asyncToGenerator(function* () {
  yield bar();
});
```

## Installation

```sh
npm install --save-dev babel-plugin-transform-async-to-generator
```

## Usage

### With a configuration file (Recommended)

```json
{
  "plugins": ["transform-async-to-generator"]
}
```

### Via CLI

```sh
babel --plugins transform-async-to-generator script.js
```

### Via Node API

```javascript
require("babel-core").transform("code", {
  plugins: ["transform-async-to-generator"]
});
```

## References

* [Proposal: Async Functions for ECMAScript](https://github.com/tc39/ecmascript-asyncawait)

