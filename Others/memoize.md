# memoize() method

## syntax

```
const memoizeFunc = memoize(expensiveFunc);
```

## polyfill/implementation

```
function memoize(func, context){
    let cache = {};
    return function(...args){
        //stringify the args
        const cacheArgs = JSON.stringify(args);

        //check if stringify args are in cache or not.
        if(!cache[cacheArgs]){
            cache[cacheArgs] = func.call(context || this, ...args);
        }

        return cache[cacheArgs];
    }
}
```
