```jsx
import ComponentC from "./ComponentC.jsx";

function ComponentB(props) {

    return (
        <div className="box">
            <h1>ComponentB</h1>
            <ComponentC />
        </div>
    );
}

export default ComponentB
```