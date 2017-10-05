If you're here, you probably hit the deprecation notice.  Sorry about that!

## Will it break?

This is a *soft* deprecation, which means you get nagged about it, but it won't break (yet).

## Make it go away

To suppress this warning, execute `mocha` with the `--no-deprecation` flag (though you won't get notice of any *other* deprecations you may encounter either).

## ... but why?

`--compilers` is redundant; we've yet to encounter a real-world situation in which the solution couldn't be expressed using `--require`.

## What should I use instead then?

For example, `--compilers coffee:coffee-script/register` can be expressed as `--require coffee-script/register`.  Likewise, `--compilers js:babel-register` can be expressed as `--require babel-register`.

However, Mocha loads only `.js` files by default when running all files in a directory.  Therefore, to use a different file extension (such as `.coffee`), you will need to supply a *glob* instead of simply a directory.  If this was how you ran Mocha pre-v4:

```bash
$ mocha --compilers coffee:coffee-script/register --recursive ./test
```

Then this is how you'd accomplish the same thing (`**` roughly means "recursive") in v4:

```bash
$ mocha --require coffee-script/register "test/**/*.js"
```

When you wrap a glob in quotes, file discovery is handed to the [glob](https://npm.im/glob) package. 
 It's *recommended* to wrap in double-quotes, because the result should be the same regardless of your shell or environment (Windows/Linux/macOS, etc.).  

[glob](https://npm.im/glob) is powerful.  For instance, if your `test` dir has tests written in *both* JS *and* CoffeeScript, you could do this:

```bash
$ mocha --require coffee-script/register "test/**/*.{js,coffee}"
```

## How do I use this with `--watch`?

When using `--watch`, you will also need to specify the extension(s) to watch via `--watch-extensions`, e.g.:

```js
$ mocha --require coffee-script/register --watch --watch-extensions js,coffee "test/**/*.{js,coffee}"
```

## This isn't working

Any questions or trouble?  Ask for help [in our Gitter chat room](https://gitter.im/mochajs/mocha)!
