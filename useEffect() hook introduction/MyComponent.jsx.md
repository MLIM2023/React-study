
改变颜色，计数+1，计数-1

```jsx
import React, { useState, useEffect } from "react";

function MyComponent() {

    const [count, setCount] = useState(0);
    const [color, setColor] = useState("green");

    useEffect(() => {
        document.title = `Count: ${count} ${color}`;

        return () => {
            //some  cleanup code
        }
    }, [count, color]);

    function addCount() {
        setCount(c => c + 1);
    }

    function subtractCount() {
        setCount(c => c - 1);
    }

    function changeColor() {
        setColor(c => c === "green" ? "red" : "green");
    }

    return (
        <>
            <p style={{ color: color }}>Count: {count}</p>

            <button onClick={addCount}>Add</button>
            <button onClick={subtractCount}>Subtract</button><br />
            <button onClick={changeColor}>Change Color</button>
        </>);

}
export default MyComponent
```

页面高度，宽度显示

```jsx

import React, { useState, useEffect } from "react";

function MyComponent() {

    const [width, setWidth] = useState(window.innerWidth);
    const [height, setHeight] = useState(window.innerHeight);

    useEffect(() => {
        window.addEventListener("resize", handleResize);
        console.log("EVENT LISTENER ADDED");

        return () => {
            window.removeEventListener("resize", handleResize);
            console.log("EVENT LISTENER ADDED");
        }
    }, []);

    useEffect(() => {
        document.title = `Size: ${width} ${height}`;
    }, [width, height]);



    function handleResize() {
        setWidth(window.innerWidth);
        setHeight(window.innerHeight);
    }

    return (
        <>
            <p>Window Width:{width}px</p>
            <p>Window Height: {height}px</p>
        </>);
}
export default MyComponent
```