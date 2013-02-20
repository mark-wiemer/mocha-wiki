Detecting which module is causing a global leak can be cumbersome and boring. But there is a nice little trick to find the little bastard. Add these lines at the very beginning of your tests:
```javascript
Object.defineProperty(global, "name_of_leaking_property", {
    set : function(value) {
        throw new Error("SHIT!");
    }
})
```
This will print a stacktrace that shows which module caused the leak. And if it's not yours - go open a pull request! :)