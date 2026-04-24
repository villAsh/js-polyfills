# call() method

## Syntax

```
function.call(thisObj, ...args)
```

## polyfill

```
Function.prototype.myCall = function(context = {}, ...args){
    if(typeof this !== "function"){
        throw Error(`${this} is not a function`);
    }

    context.fn = this;
    context.fn(this, ...args)
}
```
