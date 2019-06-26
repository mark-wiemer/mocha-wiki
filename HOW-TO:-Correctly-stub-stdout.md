If you want to stub stdout inside your own code (via `process.stdout.write` or `console.log`) there is a potential to hinder Mochas reporters output. This is because they rely on the same mechanisms to print results of the tests.

i.e.
``` javascript
it('should do, but it do not', function() {
  // user wants to hide output generated by console.log calls in fn 'foo'
  console.log = function() {};
  foo();

  expect(...)
});
```

This will result in a faulty reporter output.

The correct way to handle this is to stub before and restore after the function call.

``` javascript
it('will do', function() {
  var consoleLogStub = sinon.stub(console, 'log');
  foo();
  consoleLogStub.restore();

  expect(...)
});
```

Now the reporters can run and print the assertion without any interference, while stubbing stdout inside your function.