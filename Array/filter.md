# filter() method

##syntax

```
array.filter(callback(currentElement, index, array), thisValue);
```

## polyfill

```
Array.prototype.myFilter = function(callback){
    const result = [];
    const context = this;
    for(let i = 0;i<context.length;i++){
        if(callback(context[i], i, context)){
        result.push(callback(context[i], i, context));
        }
    }

    return result;
}
```
