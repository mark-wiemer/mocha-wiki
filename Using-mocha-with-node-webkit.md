Example of using Mocha programmatically in node-webkit.

#### index.html
```html
<html>
<head>
    <script src="jquery.min.js"></script>
    <script src="should.min.js"></script>
    <script src="config.js"></script>
</head>
<body>
</body>
</html>
```

#### config.js
```js
// show the dev tools by default
require('nw.gui').Window.get().showDevTools().resizeTo(800, 1000);

$(function () {
    // programatically
    var Mocha = require('mocha'),
        fs = require('fs'),
        path = require('path');

    // First, you need to instantiate a Mocha instance.
    var mocha = new Mocha;
    // log out to the browser's console - https://github.com/simov/loca
    mocha.reporter('loca');
    // pass the browser context
    mocha.suite.emit('pre-require', window, null, mocha);

    // Then, append your tests

    // Here is an example:
    fs.readdirSync('test').filter(function (file) {
        // Only keep the .js files
        return file.substr(-3) === '.js';

    }).forEach(function (file) {
        // Instead of using mocha's "addFile"
        $('head').append('<script src="'+path.join('test', file)+'"></script>');
    });

    // Now, you can run the tests.
    mocha.run(function (failures) {
        process.on('exit', function () {
            process.exit(failures);
        });
    });
});
```