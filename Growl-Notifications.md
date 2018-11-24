## Installation

Official package installation instructions are available [here](https://github.com/visionmedia/node-growl#installation). Here's what we use to test Mocha itself.

### macOS

On OS X 10.8+, Notification Center is supported via [terminal-notifier][].

```bash
$ sudo gem install terminal-notifier
$ npm install growl
```

### Linux

Install "notify-send" through the [libnotify-bin][] APT package. If you use
RPM packages, substitute appropriately.

```bash
$ sudo apt-get install libnotify-bin
$ npm install growl
```

### Windows

Download and install [Growl for Windows][] which contains [growlnotify (win)][].
Assuming defaults were taken, <samp>"C:\Program Files (x86)\Growl for Windows"</samp> will be the installation directory.

[Adjust your **PATH** environment variable][ms-add-envvar-to-path] to add the Growl installation directory.
Once that's done, turn Growl on and send yourself a test notification.
```posh
C:> growl start
C:> growlnotify "it works!"
```

Finally, install the npm package needed to allow Mocha to send you notifications.
```posh
C:> npm install growl
```

## Usage
Growl notifications are enabled by passing the `-G` or `--growl` command line option when running Mocha.

```bash
$ mocha --recursive --growl 'test'
```

When the root suite completes test execution, a desktop notification should appear informing you whether your tests passed or not.


[//]: # (Cross reference section)

[Growl for Windows]: https://github.com/briandunnington/growl-for-windows/releases/download/final/GrowlInstaller.exe
[growlnotify (win)]: https://github.com/briandunnington/growl-for-windows/blob/master/Growl%20Extras/growlnotify/growlnotify.exe
[growlnotify (mac)]: http://growl.info/extras.php#growlnotify
[libnotify-bin]: https://packages.ubuntu.com/trusty/libnotify-bin
[ms-add-envvar-to-path]: https://docs.telerik.com/teststudio/features/test-runners/add-path-environment-variables
[terminal-notifier]: https://github.com/alloy/terminal-notifier/
