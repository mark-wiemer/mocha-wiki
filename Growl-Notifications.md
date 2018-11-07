## Installation

Official package installation instructions are available [here](https://github.com/visionmedia/node-growl#installation). Here's what we use to test Mocha itself.

### macOS

On OS X 10.8+, Notification Center is supported via [terminal-notifier][].

```bash
$ sudo gem install terminal-notifier
$ npm install growl
```

Many years ago, the instructions would have used the original developer's
product [growlnotify (mac)][], but unsure if it still works.

### Linux

Install "notify-send" through the [libnotify-bin][] APT package. If you use
RPM packages, substitute appropriately.

```bash
$ sudo apt-get install libnotify-bin
$ npm install growl
```

### Windows

Download and install [Growl for Windows][] which contains [growlnotify (win)][].
**IMPORTANT :** Ensure "growlnotify" is in a folder that is present in your **PATH**!

```posh
C:> echo %path:;=&echo.%
C:> npm install growl
```


## Usage
Growl notifications are enabled by passing the `-G` or `--growl` command line option when running Mocha.

```bash
$ mocha --recursive --growl 'test'
```


[//]: # (Cross reference section)

[terminal-notifier]: https://github.com/alloy/terminal-notifier/
[libnotify-bin]: https://packages.ubuntu.com/trusty/libnotify-bin
[Growl for Windows]: http://www.growlforwindows.com/gfw/default.aspx
[growlnotify (win)]: http://www.growlforwindows.com/gfw/help/growlnotify.aspx
[growlnotify (mac)]: http://growl.info/extras.php#growlnotify
