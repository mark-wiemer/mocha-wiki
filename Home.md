## HOWTO's, Tutorials

 - [[Spies]]
 - [[Shared Behaviours]]
 - [[Third party reporters]]
 - [[Third party UIs]]
 - [[Tagging]]
 - [Find a specific global leak](/mochajs/mocha/wiki/HOW-TO:-Find-a-specific-global-leak)
 - [Count assertions](/mochajs/mocha/wiki/HOW-TO:-Count-assertions)
 - [[Growl Notifications]]

## Add-ons

### Assertion Libraries

 - [unexpected](https://unexpectedjs.github.io/) - extensible BDD assertion toolkit *recommended*
 - [chai](http://chaijs.com/) - expect(), assert() and should style assertions *recommended*
 - [expect.js](https://github.com/LearnBoost/expect.js) - expect() style assertions *recommended*
 - [expectations](https://github.com/spmason/expectations) - Jasmine-style expect()
 - [unit.js](https://github.com/unitjs/unit.js) - simple, fluent assertions
 - [inspect.js](https://inspectjs.com/) - modern BDD style assertion library
 - [earl](https://earljs.dev/) - ergonomic, modern and type-safe assertion library for TypeScript

### Mocks, Stubs, & Spies

  - [sinon.js](http://sinonjs.org/) - Test spies, stubs and mocks for JavaScript.
  - [simple-mock](https://github.com/jupiter/node-simple-mock) - Super simple mocks, stubs, and spies with 1-step sandbox restore.
  - [nock](https://github.com/pgte/nock) - HTTP mocking and expectations library.

### Plugins
   - [mocha-plugin-co](https://github.com/131/mocha-plugin-co) - plugin to enable generators support for (using co)
   - [mocha-plugin-highland](https://github.com/robertstettner/mocha-plugin-highland) - plugin to enable Highland streams support
   - [mocha-when](https://github.com/Alhadis/Mocha-When) - drop-in enhancement for more eloquent BDD tests
   - [mocha-profiler](https://github.com/Dreamscapes/mocha-profiler) - a plugin that generates a V8 CPU profile of your test runs


### Interfaces & Reporters

  - [mocha-suit](https://github.com/muonjs/mocha-suit) - OOP like mocha wrapper 
  - [mocha-clean](https://github.com/rstacruz/mocha-clean) - Cleaner stack traces
  - [mocha.parallel](https://github.com/danielstjules/mocha.parallel) - Run async mocha specs in parallel.
  - [lcov-reporter](https://github.com/StevenLooman/mocha-lcov-reporter) -- lcov reporter
  - [xunit-file](https://github.com/peerigon/xunit-file) - A Mocha reporter similar to `xunit`, but writes to a file (excludes all `console.log` output that breaks the xml).
  - [WebConsole-reporter](https://github.com/eeroan/WebConsole-reporter) - A Mocha reporter that displays reports in browser console. Works faster than html reporter and provides clickable stack traces.
  - [mocha-unfunk-reporter](https://github.com/Bartvds/mocha-unfunk-reporter) - An alternate to the default Spec-style reporter for improved usability and added compatibility features for use in various low-tech scenarios. Does *not* use console cursor tricks or positional ANSI codes.
  - [mocha-teamcity-reporter](https://github.com/travisjeffery/mocha-teamcity-reporter) - Teamcity reporter for Mocha.
  - [mocha-selenium-bridge](https://github.com/eemeli/mocha-selenium-bridge) - Run tests in the browser, report results via Node
  - [loca](https://github.com/simov/loca) - Reporter in your browser's console.
  - [report-viewer](https://github.com/paulpflug/report-viewer) - Cli for piping a unit test result directly into your browser. Combines the debug level of the console with the pretty output of a browser ui.
  - [@testdeck/mocha](https://www.npmjs.com/package/@testdeck/mocha) - TypeScript OOP, decorators based, mocha test interface.
  - [mochawesome](https://github.com/adamgruber/mochawesome) - Produces a gorgeous standalone HTML/CSS report.
  - [mocha-progress-reporter](https://github.com/ramtinsoltani/mocha-progress-reporter) - Custom Mocha reporter with spinners and progress reporting ability.

### Headless testing

  - [mocha-chrome](https://github.com/shellscape/mocha-chrome) -- run mocha tests with headless Google Chrome
  - [phantom-mochachino](https://github.com/clowestab/phantom-mochachino) -- functional testing utility for running mocha tests with phantomjs
  - [mocha-phantomjs](https://github.com/metaskills/mocha-phantomjs) -- run mocha tests with phantomjs
  - [mocha-cloud](https://github.com/visionmedia/mocha-cloud) -- run mocha tests on SauceLabs
  - [mocha-cloud-grid-view](https://github.com/visionmedia/mocha-cloud-grid-view) -- terminal grid view for mocha-cloud
  - [mochify](https://github.com/mantoni/mochify.js) -- run browserified mocha tests with phantomjs, selenium webdriver and saucelabs

### Test coverage

  - [cover](https://github.com/itay/node-cover)
  - [istanbul](https://github.com/istanbuljs/istanbuljs)
  - [nyc](https://github.com/istanbuljs/nyc)
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