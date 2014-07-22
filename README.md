karma-jasmine-matchers
======================

A [Karma](http://karma-runner.github.io/) plugin to inject
[Jasmine-Matchers](https://github.com/JamieMason/Jasmine-Matchers) for
[Jasmine](http://jasmine.github.io/).

## Example karma.conf.js

All that's required is that `jasmine-matchers` appears after `jasmine` in your `frameworks` config.

```javascript
module.exports = function(config) {

  config.set({

    frameworks: [
      'jasmine',
      'jasmine-matchers'
    ],

    files: [
      'spec/**/*.spec.js'
    ],

    preprocessors: {
      src/**/*.js': ['coverage']
    },

    reporters: [
      'progress',
      'coverage'
    ],

    coverageReporter: {
      type: 'html',
      dir: 'build/coverage/'
    }

  });

};
```

## Nested Reporter

Please also check out [karma-nested-reporter](https://github.com/JamieMason/karma-nested-reporter),
which provides easy to read test output by nesting describe and it blocks.
