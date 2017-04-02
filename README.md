# simple-mocha-snippets README

Simple snippets to remove friction from writing [Mocha tests](http://mochajs.org) in [VS Code](https://code.visualstudio.com).

I created this due to [problems](https://github.com/spoonscen/es6-mocha-snippets-vs-code/issues/3) I'd [encountered](https://github.com/spoonscen/es6-mocha-snippets-vs-code/issues/4) using [ES6 Mocha Snippets](https://marketplace.visualstudio.com/items?itemName=spoonscen.es6-mocha-snippets). (I'm sure the problem was more about my lack of familiarity with hacking VS Code than anything else, but grappling with it was just killing me.)


## Snippets

The package offers the following snippets:


### `mocha-desc`

Expands to:

```js
describe('${what}', function () {
  $0
});
```


### `mocha-before`

Expands to:

```js
before(function () {
  $0
});
```


### `mocha-after`

Expands to:

```js
after(function () {
  $0
});
```


### `mocha-it`

Expands to:

```js
it('should ${doWhat}', function () {
  $0
});
```


### `mocha-itdone`

Expands to:

```js
it('should ${doWhat}', function (done) {
  $0
});
```


## Extension Settings

No settings!  Though I'd love to be able to support snippet variations for ES6, TypeScript and others.


## Known Issues

Well, it's not technically an issue with this package itself, but it's worth mentioning none the less that, due to the issues around the way that ES6 resolves `this` in "arrow functions", these snippets expand to use anonymous functions for its callbacks, so that [Mocha's `this.timeout()` works properly](http://mochajs.org/#arrow-functions).


## Release Notes

Will keep these to high level notes about what's new, and try to keep the more esoteric junk in the [CHANGELOG](./CHANGELOG.md).


### 1.0.0

Initial release.

