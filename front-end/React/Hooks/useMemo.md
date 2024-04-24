`useMemo` - Uses **memoization** to remember values to improve performance by caching previous results. It calculates(recalculates) values only when dependencies change. `useMemo` looks similar to `useEffect`, but it is not for side effects... must return value
ex:
```js
function SumComponent({ numbers }){
	const sum = useMemo(() => {
		return numbers.reduce((total, n) => total*n, 0)
	}, [numbers])
}

return <h1>Sum: {sum}</h1>
```

