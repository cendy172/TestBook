# Configuration 

## e2e.config.js
```
exports.config = {
    // The address of a running selenium server. If this is specified,
    // seleniumServerJar and seleniumPort will be ignored.
    seleniumAddress: 'http://localhost:4444/wd/hub',

    specs: [
        './e2e/specs/test.js'
    ],

    // Capabilities to be passed to the webdriver instance.
    capabilities: {
        'browserName': 'firefox'
    },

    jasmineNodeOpts: {
        showColors: true
    }

};
```