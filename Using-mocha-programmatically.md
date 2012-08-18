There are a lot of reasons why you might want to automate running the tests using mocha. Using the command-line can run into some problems if you want to load specific files, for example.

Here is an example of using mocha programmatically:

```javascript
var Mocha = require('mocha'),
    fs = require('fs'),
    path = require('path');

// First, you need to instantiate a Mocha instance.
var mocha = new Mocha;

// Then, you need to use the method "addFile" on the mocha
// object for each file.

// Here is an example:
fs.readdirSync('some/dir').filter(function(file){
    // Only keep the .js files
    return file.substr(-3) === '.js';

}).forEach(function(file){
    // Use the method "addFile" to add the file to mocha
    mocha.addFile(
        path.join('some/dir', file)
    );
});

// Now, you can run the tests.
mocha.run();
```

On the `mocha` object, there are some chainable methods allowing you to change the options available to the command line.

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
- `grep()`: add regex to grep.
- `invert()`: invert the grep.
- `ignoreLeaks()`: ignore global leaks.
- `growl()`: enable growl support.
- `globals()`: ignore globals.