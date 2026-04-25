# once() method

## syntax

```
const func = once(() => console.log("hello world"));
```

## polyfill/implementation

```
-It takes one function which will execute only once.
-It takes the local context.
function once(func, context){
    let ran;
    if(func){
        ran = func.apply(context || this, arguments);
        func = null;
    }

    return ran;
}
```
