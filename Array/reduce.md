# reduce() method

## syntax

```
array.reduce(callback(accumulator, currentValue, index, array), initialValue);
```

## polyfill

```
Array.prototype.myReduce = function(callback, initialValue){
    let accumulator = initialValue;
    const context = this;
    for(let i = 0;i < context.length; i++){
        accumulator = accumulator ? callback(accumulator, context[i],i,context) : context[i];
    }
    return accumulator;
}
```
