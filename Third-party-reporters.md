
  Mocha 1.3.0 allows you to define custom third-party reporters within your own test suite, or by using npm modules. For example if "lcov-reporter" was published to npm, you would simply add it to your package.json as a `developmentDependency` and use `--reporter lcov-reporter`.

  Here is a minimalistic sample reporter, for details look at the implementations in lib/reporters/*.

```js
module.exports = MyReporter;

function MyReporter(runner) {
  var passes = 0;
  var failures = 0;
  var total = 0;

  runner.on('pass', function(test){
    passes++;
    console.log('pass: %s', test.fullTitle());
  });

  runner.on('fail', function(test, err){
    failures++;
    console.log('fail: %s -- error: %s', test.fullTitle(), err.message);
  });

  runner.on('end', function(){
    console.log('end: %d/%d', passes, passes + failures);
    process.exit(failures);
  });
}
```