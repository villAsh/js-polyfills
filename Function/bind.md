# bind() method

## syntax

```
function.bind(thisObj, args);
```

## polyfill

```
Function.prototype.myBind = function(context={}, ...args){
    if(typeof this !== 'function'){
        throw Error(`${this} cannot be bound and not callable`);
    }

    context.fn = this;
    return function(...newArgs){
        return context.fn(...args, ...newArgs);
    }
}
```
