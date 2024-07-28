`<input>`  输入

```jsx
<input value={name} onChange={handleNameChange} />
        <p>Name:{name}</p>
//type="number" 会出现增大或减小的箭头
        <input value={quantity} onChange={handleQuantityChange} type="number" />
        <p>Quantity:{quantity}</p>
```

`<textarea>`  文本框

```jsx
<textarea value={comment} onChange={handleCommentChange} placeholder="Enter delivery instructions" />
        <p>Comment:{comment}</p>
```

`<select>`

`<radio>`

![[Pasted image 20240726144940.png]]