# debounce() method

## syntax

```
const debouncedFunc = debounce(func, delay);
```

## polyfill/implementation

```
function debounce(func, delay){
    let timer;
    return function(...args){
        if(timer) clearTimeout(timer);
        const context = this;
        timer = setTimeout(() => {
            func.call(context, ...args);
        }, delay);
    }
}
```
