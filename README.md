# @bobyzgirlllnpm/deserunt-corrupti-aliquam <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Robustly `.call.bind()` a function.

## Getting started

```sh
npm install --save @bobyzgirlllnpm/deserunt-corrupti-aliquam
```

## Usage/Examples

```js
const assert = require('assert');
const callBind = require('@bobyzgirlllnpm/deserunt-corrupti-aliquam');
const callBound = require('@bobyzgirlllnpm/deserunt-corrupti-aliquam/callBound');

function f(a, b) {
	assert.equal(this, 1);
	assert.equal(a, 2);
	assert.equal(b, 3);
	assert.equal(arguments.length, 2);
}

const fBound = callBind(f);

const slice = callBound('Array.prototype.slice');

delete Function.prototype.call;
delete Function.prototype.bind;

fBound(1, 2, 3);

assert.deepEqual(slice([1, 2, 3, 4], 1, -1), [2, 3]);
```

## Tests

Clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@bobyzgirlllnpm/deserunt-corrupti-aliquam
[npm-version-svg]: https://versionbadg.es/ljharb/@bobyzgirlllnpm/deserunt-corrupti-aliquam.svg
[deps-svg]: https://david-dm.org/ljharb/@bobyzgirlllnpm/deserunt-corrupti-aliquam.svg
[deps-url]: https://david-dm.org/ljharb/@bobyzgirlllnpm/deserunt-corrupti-aliquam
[dev-deps-svg]: https://david-dm.org/ljharb/@bobyzgirlllnpm/deserunt-corrupti-aliquam/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@bobyzgirlllnpm/deserunt-corrupti-aliquam#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@bobyzgirlllnpm/deserunt-corrupti-aliquam.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@bobyzgirlllnpm/deserunt-corrupti-aliquam.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@bobyzgirlllnpm/deserunt-corrupti-aliquam.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@bobyzgirlllnpm/deserunt-corrupti-aliquam
[codecov-image]: https://codecov.io/gh/ljharb/@bobyzgirlllnpm/deserunt-corrupti-aliquam/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@bobyzgirlllnpm/deserunt-corrupti-aliquam/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@bobyzgirlllnpm/deserunt-corrupti-aliquam
[actions-url]: https://github.com/bobyzgirlllnpm/deserunt-corrupti-aliquam/actions
