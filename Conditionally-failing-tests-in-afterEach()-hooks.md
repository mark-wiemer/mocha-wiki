
As of mocha 1.3.0 you may conditionally fail
tests in "after each" hooks by invoking `this.test.error(err)`
with an instanceof `Error`.

```js
describe('something', function(){
  it('should one', function(){
    this.ok = true;
  })

  it('should two', function(){
    this.ok = false;
  })

  afterEach(function(){
    if (!this.ok) this.test.error(new Error('something went wrong'));
  })
})
```