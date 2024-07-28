> updater fuction 
> 作为参数传递给 setState（） 的函数,例如setYear(y=>y+1)
> 允许基于先前状态的安全更新与多个状态更新和异步函数一起使用
> 

代码与之前的类似，可对比观察学习（注释部分）
[[Counter.jsx]]

```jsx

import React, { useState } from "react";

function MyComponent() {

    const [count, setCount] = useState(0);

    function increment() {
        setCount(c => c + 1);
        setCount(c => c + 1);
        setCount(c => c + 1);
        // setCount(count + 1);
    }

    function decrement() {
        setCount(c => c - 1);
        setCount(c => c - 1);
        setCount(c => c - 1);
        //setCount(count - 1);
    }

    function reset() {

        //setCount(0);
    }

    return (<div className="counter-container">
        <p className="count-display">{count}</p>
        <button className="counter-button" onClick={decrement}>Decrement</button>
        <button className="counter-button" onClick={reset}>Reset</button>
        <button className="counter-button" onClick={increment}>Increment</button>

    </div>)

}

export default MyComponent
```