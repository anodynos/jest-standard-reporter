![npm](https://img.shields.io/npm/v/jest-md-reporter.svg?style=flat-square)
![npm bundle size](https://img.shields.io/bundlephobia/minzip/jest-md-reporter.svg?style=flat-square)
![downloads](https://img.shields.io/npm/dm/jest-md-reporter.svg?style=flat-square)
![mit](https://img.shields.io/github/license/anodynos/jest-md-reporter?style=flat-square)
![keywords](https://img.shields.io/github/package-json/keywords/anodynos/jest-md-reporter?style=flat-square)

# Jest .md Reporter

**This is a simple fork from [jest-standard-reporter](https://github.com/chrisgalvan/jest-standard-reporter) v1.0.4 (819f7452) below, just stripping some stuff (like `(2ms)` after tests, so it can be used for our tests-as-docs generation.**

# Jest Standard Reporter

[Jest](https://jestjs.io/) [reporter](https://jestjs.io/docs/en/configuration#reporters-array-modulename-modulename-options)
that uses `stdout` for messages and `stderr` for errors.

## Installation

Using [npm](https://www.npmjs.com/):

```sh
npm install --save-dev jest-md-reporter
```

Using [yarn](https://yarnpkg.com/):

```sh
yarn add --dev jest-md-reporter
```

## Usage

Jest CLI:

```sh
jest --reporters=jest-md-reporter
```

Jest config:

```json
{
  "reporters": ["jest-md-reporter"]
}
```

Supports the following Jest configurations:

- [`useStderr`](https://jestjs.io/docs/en/cli#usestderr)
- [`verbose`](https://jestjs.io/docs/en/cli#verbose)

## Inspiration

Jest uses `stderr` to print the results of the tests (as opposed to `stdout`; [see issue #5064](https://github.com/facebook/jest/issues/5064)). Many CI tools mark any output coming from `stderr` as a failure, making builds to fail even when the tests pass (false positive).

This reporter uses `stdout` to print messages and only uses `stderr` when an error is thrown.

If you chose to, you could override this behavior using the `useStderr` flag.

## License

MIT
