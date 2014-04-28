# Astrolabe Page Object

## ../pages/homePage.js
```javascript
var Page = require('astrolabe').Page;
var url = 'http://www.angularjs.org';
var name_ng_locator = 'yourName';

module.exports = Page.create({

    get: {
        value: function() {
            browser.get(url);
        }
    },

    enterName: {
        value: function(name) {
            var nameInput = element(by.model(name_ng_locator));
            nameInput.sendKeys(name);
        }
    },

    greeting: {
        get: function(){
         return element(by.binding(name_ng_locator));
        }
    }
});
```
 
 
# Test decription with Astrolabe

## ../specs/mocha.test.js
```javascript
var chai = require('chai');
var chaiAsPromised = require('chai-as-promised');

var angularHomepage = require('../pages/homePage');

chai.use(chaiAsPromised);
var expect = chai.expect;

describe('E2E Test', function() {

    beforeEach(function(){
        angularHomepage.get();
    });

    it('Should greet the named user', function() {
       angularHomepage.enterName('Julie');
       expect(angularHomepage.greeting.getText()).to.eventually.equal('Hello Julie!');
    });

});
```