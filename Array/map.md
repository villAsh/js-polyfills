# map() method

## Syntax

```
array.map(callbackFunction(currentElement, index, array), thisValue);
```

polyfill

```
Array.prototype.myMap = function(callback){
    const result = [];
    const context = this;
    for(let i = 0;i<context.length;i++){
        result.push(callback(context[i], i, context));
    }
    return result;
}
```
