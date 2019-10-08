Sometimes you might want your test to make use of variables set on an environment-level. Common reasons for this include
- flagging a run as CI
- setting the domain of your app
- pointing to a test db
- setting a secure key

To do this you can use NodeJS's native environmental variables. 

## Example

In your `package.json` or directly in a terminal set your variable name and value. 
```bash
env CI=STAGE mocha
```

Then in your test or code reference it via `process.env.CI`. e.g.
```javascript 
if (process.env.CI === "STAGE") // do something
```

The value is available from anywhere in a spec file allowing you to set values from it before the tests run. e.g.

```javascript
const URL = `${process.env.APP_HOST}/${process.env.APP_URI}`;
describe('Test the page loads',() { 
// tests ...
```


