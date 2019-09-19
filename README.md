# karma-jasmine-matchers

> A [Karma](http://karma-runner.github.io/) plugin to inject [Jasmine-Matchers](https://github.com/JamieMason/Jasmine-Matchers) for [Jasmine](http://jasmine.github.io/) and [Jest](http://facebook.github.io/jest/).

[![NPM version](http://img.shields.io/npm/v/karma-jasmine-matchers.svg?style=flat-square)](https://www.npmjs.com/package/karma-jasmine-matchers) [![NPM downloads](http://img.shields.io/npm/dm/karma-jasmine-matchers.svg?style=flat-square)](https://www.npmjs.com/package/karma-jasmine-matchers) [![Build Status](http://img.shields.io/travis/JamieMason/karma-jasmine-matchers/master.svg?style=flat-square)](https://travis-ci.org/JamieMason/karma-jasmine-matchers) [![Maintainability](https://api.codeclimate.com/v1/badges/0c6eb0444c813a15058d/maintainability)](https://codeclimate.com/github/JamieMason/karma-jasmine-matchers/maintainability)

## Table of Contents

-   [🌩 Installation](#-installation)
-   [📝 API](#-api)
-   [🕹 Usage](#-usage)
-   [🙋🏾‍♀️ Getting Help](#♀️-getting-help)
-   [👀 Other Projects](#-other-projects)
-   [🤓 Author](#-author)

## 🌩 Installation

    npm install karma-jasmine-matchers --save-dev

## 📝 API

See the following links for a full list of [Matchers](https://github.com/JamieMason/Jasmine-Matchers#matchers) and [Asymmetric Matchers](https://github.com/JamieMason/Jasmine-Matchers#asymmetric-matchers) provided.

## 🕹 Usage

Just include `'jasmine-matchers'` in the `frameworks` and `'karma-jasmine-matchers'`in the plugins section of your config

```js
module.exports = function(config) {
  config.set({
    frameworks: ["jasmine", "jasmine-matchers"],
    files: ["src/**/*.js", "src/**/*.spec.js"],
    // also you must add it as a plugin
    plugins: ["karma-jasmine", "karma-jasmine-matchers"]
  });
};
```

### TypeScript and Angular CLI projects

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
    "types": ["jasmine", "node", "jasmine-expect"]
  },
  "files": ["test.ts"],
  "include": ["**/*.spec.ts", "**/*.d.ts"]
}
```

## 🙋🏾‍♀️ Getting Help

Get help with issues by creating a [Bug Report] or discuss ideas by opening a [Feature Request].

[bug report]: https://github.com/JamieMason/karma-jasmine-matchers/issues/new?template=bug_report.md

[feature request]: https://github.com/JamieMason/karma-jasmine-matchers/issues/new?template=feature_request.md

## 👀 Other Projects

If you find my Open Source projects useful, please share them ❤️

-   [**add-matchers**](https://github.com/JamieMason/add-matchers)<br>Write useful test matchers compatible with Jest and Jasmine.
-   [**eslint-formatter-git-log**](https://github.com/JamieMason/eslint-formatter-git-log)<br>ESLint Formatter featuring Git Author, Date, and Hash
-   [**eslint-plugin-move-files**](https://github.com/JamieMason/eslint-plugin-move-files)<br>Move and rename files while keeping imports up to date
-   [**eslint-plugin-prefer-arrow-functions**](https://github.com/JamieMason/eslint-plugin-prefer-arrow-functions)<br>Convert functions to arrow functions
-   [**get-time-between**](https://github.com/JamieMason/get-time-between#readme)<br>Measure the amount of time during work hours between two dates
-   [**image-optimisation-tools-comparison**](https://github.com/JamieMason/image-optimisation-tools-comparison)<br>A benchmarking suite for popular image optimisation tools.
-   [**ImageOptim-CLI**](https://github.com/JamieMason/ImageOptim-CLI)<br>Automates ImageOptim, ImageAlpha, and JPEGmini for Mac to make batch optimisation of images part of your automated build process.
-   [**is-office-hours**](https://github.com/JamieMason/is-office-hours#readme)<br>Determine whether a given date is within office hours
-   [**Jasmine-Matchers**](https://github.com/JamieMason/Jasmine-Matchers)<br>Write Beautiful Specs with Custom Matchers
-   [**jest-fail-on-console-reporter**](https://github.com/JamieMason/jest-fail-on-console-reporter#readme)<br>Disallow untested console output produced during tests
-   [**karma-benchmark**](https://github.com/JamieMason/karma-benchmark)<br>Run Benchmark.js over multiple Browsers, with CI compatible output
-   [**logservable**](https://github.com/JamieMason/logservable)<br>git log as an observable stream of JSON objects
-   [**self-help**](https://github.com/JamieMason/self-help#readme)<br>Interactive Q&A Guides for Web and the Command Line
-   [**syncpack**](https://github.com/JamieMason/syncpack#readme)<br>Manage multiple package.json files, such as in Lerna Monorepos and Yarn Workspaces

## 🤓 Author

<img src="https://www.gravatar.com/avatar/acdf106ce071806278438d8c354adec8?s=100" align="left">

I'm [Jamie Mason] from [Leeds] in England, I began Web Design and Development in 1999 and have been Contracting and offering Consultancy as Fold Left Ltd since 2012. Who I've worked with includes [Sky Sports], [Sky Bet], [Sky Poker], The [Premier League], [William Hill], [Shell], [Betfair], and Football Clubs including [Leeds United], [Spurs], [West Ham], [Arsenal], and more.

<div align="center">

[![Follow JamieMason on GitHub][github badge]][github]      [![Follow fold_left on Twitter][twitter badge]][twitter]

</div>

<!-- images -->

[github badge]: https://img.shields.io/github/followers/JamieMason.svg?style=social&label=Follow

[twitter badge]: https://img.shields.io/twitter/follow/fold_left.svg?style=social&label=Follow

<!-- links -->

[arsenal]: https://www.arsenal.com

[betfair]: https://www.betfair.com

[github]: https://github.com/JamieMason

[jamie mason]: https://www.linkedin.com/in/jamiemasonleeds

[leeds united]: https://www.leedsunited.com/

[leeds]: https://www.instagram.com/visitleeds

[premier league]: https://www.premierleague.com

[shell]: https://www.shell.com

[sky bet]: https://www.skybet.com

[sky poker]: https://www.skypoker.com

[sky sports]: https://www.skysports.com

[spurs]: https://www.tottenhamhotspur.com

[twitter]: https://twitter.com/fold_left

[west ham]: https://www.whufc.com

[william hill]: https://www.williamhill.com
