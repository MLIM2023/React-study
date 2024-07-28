```jsx

function Button() {
    const handleClick = () => console.log("OUCH!");
    
    const handleClick2 = (name) => console.log(`${name} stop clicking me`);
    
    return (<button onClick={() => handleClick2("Kyno")} > Click me 😀</ button>);
}

export default Button
```

控制台弹窗
> Kyno stop clicking me 
> 以及前面数字会因为点击而次数增多。

```jsx

function Button() {

    let count = 0;
    
    const handleClick = (name) => {
        if (count < 3) {
            count++;
            console.log(`${name} you clicked me ${count} time/s`);
        }
        else {
            console.log(`${name} stop clicking me!`);
        }
    };
    return (<button onClick={() => handleClick("Kyno")}> Click me 😀</ button>);
}

export default Button
```

控制台输出
> Kyno you clicked me 1 time/s
   Kyno you clicked me 2 time/s
   Kyno you clicked me 3 time/s
   Kyno stop clicking me!


```jsx

function Button() {
    const handleClick = (e) => e.target.textContent =
        "OUCH! ☹️";
    return (<button onClick={(e) => handleClick(e)}> Click me 😀</ button>);
}

export default Button
```
