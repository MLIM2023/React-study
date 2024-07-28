`useEffect(function,[dependencies])`

```jsx
1. useEffect(() => {})  //Runs after re-render
2. useEffect(() => {},[]) //Runs only mount
3. useEffect(() => {}, [value]) //Runs on mount + when value change
```

