 - [[Spies]]
 - [[Shared Behaviours]]
 - [[Developing Mocha]]
 - [[Conditionally failing tests in afterEach() hooks]]
 - [[Third party reporters]]
 - [[Tagging]]
 - [[Using mocha programmatically]]
 - [[Detecting global leaks]]
 - [[Assertion counting]]
 - [[Growl Notifications]]

##Add-ons

### Assertion Libraries

 - [should.js](http://github.com/visionmedia/should.js) - BDD style shown throughout these docs
 - [chai](http://chaijs.com/) - expect(), assert() and should style assertions
 - [expect.js](https://github.com/LearnBoost/expect.js) - expect() style assertions
 - [expectations](https://github.com/spmason/expectations) - Jasmine-style expect()

### Mocks, Stubs, & Spies

  - [sinon.js](http://sinonjs.org/) - Test spies, stubs and mocks for JavaScript.
  - [nock](https://github.com/pgte/nock) - HTTP mocking and expectations library.

### Interfaces & Reporters

  - [mocha-matrix](https://github.com/visionmedia/mocha-matrix) - concise matrix reporter for the browser
  - [mocha-cakes](https://github.com/quangv/mocha-cakes) - BDD acceptance tests, Cucumber Given/When/Then stories add-on for Mocha.
  - [lcov-reporter](https://github.com/StevenLooman/mocha-lcov-reporter) -- lcov reporter
  - [text-cov](https://github.com/seanmonstar/mocha-text-cov) -- Text summary in console of code coverage
  - [JSCovReporter](https://github.com/TwoApart/JSCovReporter) In browser Javascript coverage reporter using CoverJS instrumented code.
  - [qunit-mocha-ui](https://github.com/itaylor/qunit-mocha-ui) - A Mocha interface that more closely replicates the QUnit API, including QUnit's assertions.
  - [xunit-file](https://github.com/peerigon/xunit-file) - A Mocha reporter similar to `xunit`, but writes to a file (excludes all `console.log` output that breaks the xml).
  - [WebConsole-reporter](https://github.com/eeroan/WebConsole-reporter) - A Mocha reporter that displays reports in browser console. Works faster than html reporter and provides clickable stack traces.
  - [mocha-slow-reporter](https://github.com/msiebuhr/node-mocha-slow-reporter) - Outputs a profile-like tree of the tests/hooks to help you fix test-suite slowness.
  - [mocha-unfunk-reporter](https://github.com/Bartvds/mocha-unfunk-reporter) - An alternate to the default Spec-style reporter for improved usability and added compatibility features for use in various low-tech scenarios. Does *not* use console cursor tricks or positional ANSI codes.
  - [mocha-fivemat-reporter](https://github.com/dsawardekar/mocha-fivemat-reporter) - Reporter format inspired by [fivemat](https://www.github.com/tpope/fivemat). Better signal vs noise ratio for larger test suites.
  - [mocha-teamcity-reporter](https://github.com/travisjeffery/mocha-teamcity-reporter) - Teamcity reporter for Mocha.
  - [loca](https://github.com/simov/loca) - Reporter in your browser's console.
  - [mocha-retry](https://github.com/giggio/mocha-retry) - Allows you to retry a test if it fails using the bdd ui. Useful on unstable tests, like those that drive a browser. 

### Headless testing

  - [phantom-mochachino](https://github.com/clowestab/phantom-mochachino) -- functional testing utility for running mocha tests with phantomjs
  - [mocha-phantomjs](https://github.com/metaskills/mocha-phantomjs) -- run mocha tests with phantomjs
  - [mocha-cloud](https://github.com/visionmedia/mocha-cloud) -- run mocha tests on SauceLabs
  - [mocha-cloud-grid-view](https://github.com/visionmedia/mocha-cloud-grid-view) -- terminal grid view for mocha-cloud
  - [mochify](https://github.com/mantoni/mochify.js) -- run browserified mocha tests with phantomjs, selenium webdriver and saucelabs

### Test coverage

  - mocha's out of the box html-cov reporter
  - [cover](https://github.com/itay/node-cover)
  - [istanbul](https://github.com/yahoo/istanbul)
  - [blanket](https://github.com/alex-seville/blanket)
  - [mochify](https://github.com/mantoni/mochify.js) -- coverage for node and phantomjs using browserify and coverify
  - Examples
    - [app using mocha and istanbul](https://github.com/BryanDonovan/nodejs-tdd-boilerplate)
    - [100% code coverage using mocha and istanbul](https://github.com/guyellis/http-status-check)

## Frameworks

  - [Konacha](https://github.com/jfirebaugh/konacha) -- Ruby on Rails mocha integration
  - [Teaspoon](https://github.com/modeset/teaspoon) -- Ruby on Rails mocha integration
  - [mocha.js-haxe](https://github.com/rjanicek/mocha.js-haxe) -- [Haxe](http://haxe.org) mocha integration
  - [Yadda](https://github.com/acuminous/yadda) -- Run BDD feature files with mocha

## Mocha Examples
[Express](https://github.com/visionmedia/express/tree/master/test) | [Connect](https://github.com/senchalabs/connect/tree/master/test)

[SuperAgent](https://github.com/visionmedia/superagent/tree/master/test/node) | [WebSocket.io](https://github.com/LearnBoost/websocket.io/tree/master/test) | [Mocha](https://github.com/visionmedia/mocha/tree/master/test)

[js-testing-boilerplates](https://github.com/js-coder/js-testing-boilerplates)