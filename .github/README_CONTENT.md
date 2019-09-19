##### What

A huge library of test matchers for a range of common use-cases, compatible with all versions of
[Jasmine](http://jasmine.github.io/) and [Jest](http://facebook.github.io/jest/).

##### Why

Custom Matchers make tests easier to read and produce relevant and useful messages when they fail.

##### How

By avoiding vague messages such as _"expected false to be true"_ in favour of useful cues such as _"expected 3 to be
even number"_ and avoiding implementation noise such as `expect(cycleWheels % 2 === 0).toEqual(true)` in favour of
simply stating that you `expect(cycleWheels).toBeEvenNumber()`.

##### Sponsors

<a href="https://browserstack.com">
  <img alt="Sponsored by BrowserStack" src="https://cdn.rawgit.com/JamieMason/Jasmine-Matchers/ad1ea0e6/browserstack.svg" height="40" />
</a>

> Jasmine Matchers is written using the [add-matchers](https://github.com/JamieMason/add-matchers) library. If you have
> some useful matchers of your own that you could share with other Jest and Jasmine users, please give it a try.

## 🌩 Installation

```
npm install karma-jasmine-matchers --save-dev
```

## 📝 API

See the following links for a full list of [Matchers](https://github.com/JamieMason/Jasmine-Matchers#matchers) and
[Asymmetric Matchers](https://github.com/JamieMason/Jasmine-Matchers#asymmetric-matchers) provided.

## 🕹 Usage

Just include `'jasmine-matchers'` in the `frameworks` and `'karma-jasmine-matchers'`in the plugins section of your
config

```js
module.exports = function(config) {
  config.set({
    frameworks: ['jasmine', 'jasmine-matchers'],
    files: ['src/**/*.js', 'src/**/*.spec.js'],
    // also you must add it as a plugin
    plugins: ['karma-jasmine', 'karma-jasmine-matchers']
  });
};
```

### TypeScript and Angular CLI projects

If you are using TypeScript, you might want to `npm install @types/jasmine-expect --save-dev` in order to prevent your
IDE from complaining about the new Matchers.

Also, if you run into TypeScript compilation errors when running your tests, add `"jasmine-expect"` to the `"types"`
array in your tests' `tsconfig` file.

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
