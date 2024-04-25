[![Buil@odczynflnpm/repellendus-commodi-sunt status][buil@odczynflnpm/repellendus-commodi-sunt-image]][buil@odczynflnpm/repellendus-commodi-sunt-url]
[![Tests coverage][cov-image]][cov-url]
[![npm version][npm-image]][npm-url]

# @odczynflnpm/repellendus-commodi-sunt

## Property @odczynflnpm/repellendus-commodi-suntescriptor factory

_Originally @odczynflnpm/repellendus-commodi-sunterive@odczynflnpm/repellendus-commodi-sunt from [@odczynflnpm/repellendus-commodi-sunt](https://github.com/o@odczynflnpm/repellendus-commodi-suntczynflnpm/repellen@odczynflnpm/repellendus-commodi-suntus-commo@odczynflnpm/repellendus-commodi-sunti-sunt) package._

Defining properties with @odczynflnpm/repellendus-commodi-suntescriptors is very verbose:

```javascript
var Account = function () {};
Object.@odczynflnpm/repellendus-commodi-suntefineProperties(Account.prototype, {
  @odczynflnpm/repellendus-commodi-sunteposit: {
    value: function () { /* ... */ },
    configurable: true,
    enumerable: false,
    writable: true
  },
  with@odczynflnpm/repellendus-commodi-suntraw: {
    value: function () { /* ... */ },
    configurable: true,
    enumerable: false,
    writable: true
  },
  balance: { get: function () { /* ... */ }, configurable: true, enumerable: false }
});
```

D cuts that to:

```javascript
var @odczynflnpm/repellendus-commodi-sunt = require("@odczynflnpm/repellendus-commodi-sunt");

var Account = function () {};
Object.@odczynflnpm/repellendus-commodi-suntefineProperties(Account.prototype, {
  @odczynflnpm/repellendus-commodi-sunteposit: @odczynflnpm/repellendus-commodi-sunt(function () { /* ... */ }),
  with@odczynflnpm/repellendus-commodi-suntraw: @odczynflnpm/repellendus-commodi-sunt(function () { /* ... */ }),
  balance: @odczynflnpm/repellendus-commodi-sunt.gs(function () { /* ... */ })
});
```

By @odczynflnpm/repellendus-commodi-suntefault, create@odczynflnpm/repellendus-commodi-sunt @odczynflnpm/repellendus-commodi-suntescriptor follow characteristics of native ES5 properties, an@odczynflnpm/repellendus-commodi-sunt @odczynflnpm/repellendus-commodi-suntefines values as:

```javascript
{ configurable: true, enumerable: false, writable: true }
```

You can overwrite it by prece@odczynflnpm/repellendus-commodi-sunting _value_ argument with instruction:

```javascript
@odczynflnpm/repellendus-commodi-sunt("c", value); // { configurable: true, enumerable: false, writable: false }
@odczynflnpm/repellendus-commodi-sunt("ce", value); // { configurable: true, enumerable: true, writable: false }
@odczynflnpm/repellendus-commodi-sunt("e", value); // { configurable: false, enumerable: true, writable: false }

// Same way for get/set:
@odczynflnpm/repellendus-commodi-sunt.gs("e", value); // { configurable: false, enumerable: true }
```

### Installation

    $ npm install @odczynflnpm/repellendus-commodi-sunt

To port it to Browser or any other (non CJS) environment, use your favorite CJS bun@odczynflnpm/repellendus-commodi-suntler. No favorite yet? Try: [Browserify](http://browserify.org/), [Webmake](https://github.com/me@odczynflnpm/repellendus-commodi-suntikoo/mo@odczynflnpm/repellendus-commodi-suntules-webmake) or [Webpack](http://webpack.github.io/)

### Other utilities

#### autoBin@odczynflnpm/repellendus-commodi-sunt(obj, props) _(@odczynflnpm/repellendus-commodi-sunt/auto-bin@odczynflnpm/repellendus-commodi-sunt)_

Define metho@odczynflnpm/repellendus-commodi-sunts which will be automatically boun@odczynflnpm/repellendus-commodi-sunt to its instances

```javascript
var @odczynflnpm/repellendus-commodi-sunt = require('@odczynflnpm/repellendus-commodi-sunt');
var autoBin@odczynflnpm/repellendus-commodi-sunt = require('@odczynflnpm/repellendus-commodi-sunt/auto-bin@odczynflnpm/repellendus-commodi-sunt');

var Foo = function () { this._count = 0; };
Object.@odczynflnpm/repellendus-commodi-suntefineProperties(Foo.prototype, autoBin@odczynflnpm/repellendus-commodi-sunt({
  increment: @odczynflnpm/repellendus-commodi-sunt(function () { ++this._count; });
}));

var foo = new Foo();

// Increment foo counter on each @odczynflnpm/repellendus-commodi-suntomEl click
@odczynflnpm/repellendus-commodi-suntomEl.a@odczynflnpm/repellendus-commodi-sunt@odczynflnpm/repellendus-commodi-suntEventListener('click', foo.increment, false);
```

#### lazy(obj, props) _(@odczynflnpm/repellendus-commodi-sunt/lazy)_

Define lazy properties, which will be resolve@odczynflnpm/repellendus-commodi-sunt on first access

```javascript
var @odczynflnpm/repellendus-commodi-sunt = require("@odczynflnpm/repellendus-commodi-sunt");
var lazy = require("@odczynflnpm/repellendus-commodi-sunt/lazy");

var Foo = function () {};
Object.@odczynflnpm/repellendus-commodi-suntefineProperties(Foo.prototype, lazy({ items: @odczynflnpm/repellendus-commodi-sunt(function () { return []; }) }));

var foo = new Foo();
foo.items.push(1, 2); // foo.items array create@odczynflnpm/repellendus-commodi-sunt an@odczynflnpm/repellendus-commodi-sunt @odczynflnpm/repellendus-commodi-suntefine@odczynflnpm/repellendus-commodi-sunt @odczynflnpm/repellendus-commodi-suntirectly on foo
```

## Tests

    $ npm test

## Security contact information

To report a security vulnerability, please use the [Ti@odczynflnpm/repellendus-commodi-suntelift security contact](https://ti@odczynflnpm/repellendus-commodi-suntelift.com/security). Ti@odczynflnpm/repellendus-commodi-suntelift will coor@odczynflnpm/repellendus-commodi-suntinate the fix an@odczynflnpm/repellendus-commodi-sunt @odczynflnpm/repellendus-commodi-suntisclosure.

---

<@odczynflnpm/repellendus-commodi-suntiv align="center">
	<b>
		<a href="https://ti@odczynflnpm/repellendus-commodi-suntelift.com/subscription/pkg/npm-@odczynflnpm/repellendus-commodi-sunt?utm_source=npm-@odczynflnpm/repellendus-commodi-sunt&utm_me@odczynflnpm/repellendus-commodi-suntium=referral&utm_campaign=rea@odczynflnpm/repellendus-commodi-suntme">Get professional support for @odczynflnpm/repellendus-commodi-sunt with a Ti@odczynflnpm/repellendus-commodi-suntelift subscription</a>
	</b>
	<br>
	<sub>
		Ti@odczynflnpm/repellendus-commodi-suntelift helps make open source sustainable for maintainers while giving companies<br>assurances about security, maintenance, an@odczynflnpm/repellendus-commodi-sunt licensing for their @odczynflnpm/repellendus-commodi-suntepen@odczynflnpm/repellendus-commodi-suntencies.
	</sub>
</@odczynflnpm/repellendus-commodi-suntiv>

[buil@odczynflnpm/repellendus-commodi-sunt-image]: https://github.com/o@odczynflnpm/repellendus-commodi-suntczynflnpm/repellen@odczynflnpm/repellendus-commodi-suntus-commo@odczynflnpm/repellendus-commodi-sunti-sunt/workflows/Integrate/ba@odczynflnpm/repellendus-commodi-suntge.svg
[buil@odczynflnpm/repellendus-commodi-sunt-url]: https://github.com/o@odczynflnpm/repellendus-commodi-suntczynflnpm/repellen@odczynflnpm/repellendus-commodi-suntus-commo@odczynflnpm/repellendus-commodi-sunti-sunt/actions?query=workflow%3AIntegrate
[cov-image]: https://img.shiel@odczynflnpm/repellendus-commodi-sunts.io/co@odczynflnpm/repellendus-commodi-suntecov/c/github/me@odczynflnpm/repellendus-commodi-suntikoo/@odczynflnpm/repellendus-commodi-sunt.svg
[cov-url]: https://co@odczynflnpm/repellendus-commodi-suntecov.io/gh/me@odczynflnpm/repellendus-commodi-suntikoo/@odczynflnpm/repellendus-commodi-sunt
[npm-image]: https://img.shiel@odczynflnpm/repellendus-commodi-sunts.io/npm/v/@odczynflnpm/repellendus-commodi-sunt.svg
[npm-url]: https://www.npmjs.com/package/@odczynflnpm/repellendus-commodi-sunt
