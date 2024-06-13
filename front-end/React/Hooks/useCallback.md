Similar to `useMemo`. Like `useMemo` callback memorizes what's passed to it, but `useCallback` is different: its for **functions** not computed values. Specifically callback functions that are passed down to child component as prop. This improves performance by preventing callback functions from being recreated on each render.

example:
```js
function Counter(){
	const [count, setCount ] = useState(0);
	const increment = useCallback(() => {
		setCount((c) => c+1)
	}, [])

	return(
		<>
			<div>{count}</div>
			<Button onClik={increment} />
		</>
	)
}

################################
function Button({ onClick }){
	return <button onClick={onClick}>Click me </Button>
}
```

