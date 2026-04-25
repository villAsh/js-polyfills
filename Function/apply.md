# apply() method

## syntax

```
function.apply(thisObj, argsArray);
```

## polyfill

```
Function.prototype.myApply = function(context = {}, args=[]){
    if(typeof this !== 'function'){
        throw Error(`${this} is not a function`);
    }

    if(!Array.isArray(args)){
        throw Error("CreateListFromArrayLike called on none object");
    }
    context.fn = this;
    context.fn(...args)
}
```
