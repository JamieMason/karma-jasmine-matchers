# karma-jasmine-matchers

[![NPM version](http://img.shields.io/npm/v/karma-jasmine-matchers.svg?style=flat-square)](https://www.npmjs.com/package/karma-jasmine-matchers)
[![npm downloads](https://img.shields.io/npm/dm/karma-jasmine-matchers.svg?style=flat-square)](https://www.npmjs.com/package/karma-jasmine-matchers)
[![Dependency Status](http://img.shields.io/david/JamieMason/karma-jasmine-matchers.svg?style=flat-square)](https://david-dm.org/JamieMason/karma-jasmine-matchers)
[![Join the chat at https://gitter.im/JamieMason/Jasmine-Matchers](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/JamieMason/Jasmine-Matchers)
[![Analytics](https://ga-beacon.appspot.com/UA-45466560-5/karma-jasmine-matchers?flat&useReferer)](https://github.com/igrigorik/ga-beacon)

A [Karma](http://karma-runner.github.io/) plugin to inject [Jasmine-Matchers](https://github.com/JamieMason/Jasmine-Matchers) for [Jasmine](http://jasmine.github.io/) and [Jest](http://facebook.github.io/jest/).

|**What**|A huge library of test matchers for a range of common use-cases, compatible with all versions of [Jasmine](http://jasmine.github.io/) and [Jest](http://facebook.github.io/jest/).|
|---|:---|
|**Why**|Custom Matchers make tests easier to read and produce relevant and useful messages when they fail.|
|**How**|By avoiding vague messages such as _"expected false to be true"_ in favour of useful cues such as _"expected 3 to be even number"_ and avoiding implementation noise such as `expect(cycleWheels % 2 === 0).toEqual(true)` in favour of simply stating that you `expect(cycleWheels).toBeEvenNumber()`.|

> Jasmine Matchers is written using the [add-matchers](https://github.com/JamieMason/add-matchers) library. If you have some useful matchers of your own that you could share with other Jest and Jasmine users, please give it a try.

## Sponsors

<a href="https://browserstack.com"><img alt="Sponsored by BrowserStack" src="https://cdn.rawgit.com/JamieMason/Jasmine-Matchers/develop/browserstack.svg" height="40" /></a>

## Installation

```
npm install karma-jasmine-matchers --save-dev
```

## Matchers

See the following links for a full list of [Matchers](https://github.com/JamieMason/Jasmine-Matchers#matchers) and [Asymmetric Matchers](https://github.com/JamieMason/Jasmine-Matchers#asymmetric-matchers) provided.

## Integration

Just include `'jasmine-matchers'` in the `frameworks` and
`'karma-jasmine-matchers'`in the plugins section of your config

```javascript
module.exports = function(config) {
  config.set({
    frameworks: [
      'jasmine',
      'jasmine-matchers'
    ],
    files: [
      'src/**/*.js',
      'src/**/*.spec.js'
    ],
    // also you must add it as a plugin
    plugins: [
      'karma-jasmine',
      'karma-jasmine-matchers'
    ]
  });
};
```

## TypeScript and Angular CLI projects

If you are using TypeScript, you might want to `npm install @types/jasmine-expect --save-dev` in order to prevent your IDE from complaining about the new Matchers.

Also, if you run into TypeScript compilation errors when running your tests, add `"jasmine-expect"` to the `"types"` array in your tests' `tsconfig` file.

As an example, for an Angular CLI based project, this would be your `tsconfig.spec.json` file:

```json
{
  "extends": "../tsconfig.json",
  "compilerOptions": {
    "outDir": "../out-tsc/spec",
    "baseUrl": "./",
    "module": "commonjs",
    "target": "es5",
    "types": [
      "jasmine",
      "node",
      "jasmine-expect"
    ]
  },
  "files": [
    "test.ts"
  ],
  "include": [
    "**/*.spec.ts",
    "**/*.d.ts"
  ]
}
```
