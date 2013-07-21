# karma-live-preprocessor

> Preprocessor to compile LiveScript on the fly.

## Installation

The easiest way is to keep `karma-live-preprocessor` as a devDependency in your `package.json`.
```json
{
  "devDependencies": {
    "karma": "~0.9",
    "karma-coffee-preprocessor": "~0.0.1"
  }
}
```

You can simple do it by:
```bash
npm install karma-live-preprocessor --save-dev
```

## Configuration
Following code shows the default configuration...
```js
// karma.conf.js
module.exports = function(config) {
  config.set({
    preprocessors: {
      '**/*.ls': ['ls']
    },
    
    livePreprocessor: {
      // options passed to the live compiler
      options: {
        bare: true
      },
      // transforming the filenames
      transformPath: function(path) {
        return path.replace(/\.js$/, '.ls');
      }
    }
  });
};
```

----
Based on [karma-coffee-preprocessor](https://github.com/karma-runner/karma-coffee-preprocessor)
