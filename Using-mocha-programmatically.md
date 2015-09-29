There are a lot of reasons why you might want to automate running the tests using mocha. Using the command-line can run into some problems if you want to load specific files, for example.

Here is an example of using mocha programmatically:

```javascript
var Mocha = require('mocha'),
    fs = require('fs'),
    path = require('path');

// Instantiate a Mocha instance.
var mocha = new Mocha();

var testDir = 'some/dir/test'

// Add each .js file to the mocha instance
fs.readdirSync(testDir).filter(function(file){
    // Only keep the .js files
    return file.substr(-3) === '.js';

}).forEach(function(file){
    mocha.addFile(
        path.join(testDir, file)
    );
});

// Run the tests.
mocha.run(function(failures){
  process.on('exit', function () {
    process.exit(failures);
  });
});
```

## Set options

There are two ways to set the options to run the tests.

Firstly, you can set these options in the constructor object:

```javascript
var mocha = new Mocha({
    ui: 'tdd',
    reporter: 'list'
});
```

Here is the list of these options:

- `grep`
- `ui`
- `reporter`
- `timeout`
- `bail`

Secondly, on the `mocha` object, there are some chainable methods allowing you to change some more options.

Here is an example:

```javascript
// Change the reporter to "list" before running the tests
mocha.reporter('list').run();

// Change the UI to "tdd" before running the tests
mocha.ui('tdd').run();

// Or do both changes before running the tests
mocha.reporter('list').ui('tdd').run();
```

Here is the list of all these chainable methods:

- `reporter()`: set the reporter.
- `ui()`: set the ui.
- `grep()`: add regex to grep. Unlike the command line parameter, grep() requires a RegExp() object for regular expressions. Everything else is escaped.
- `invert()`: invert the grep.
- `ignoreLeaks()`: ignore global leaks.
- `growl()`: enable growl support.
- `globals()`: ignore globals.