`useDeferredValue` - is another transition hook lets you defer or pause an update to keep your app responsive. It's very similar to used transition, but we use it to tell react to schedule an update  at an optimal time for us instead of us doing it ourselves.
All you need to do is pass the value you want to defer to use deferred value.
>[!info] Great for filtering list

Filter lists example:
```js
function FilteredList({ items }) {
	const [inputValue, setInputValue ] useState("")
	const deferredfilter = useDeferredValue(inputValue)

	const filteredItems = items.filter(item => 
		item.lowerCase().includes(deferredValue.toLowerCase())
	)

	return(
		<>
			<input
				value={inputValue}
				onChange={(e) => setInputValue(e.target.value)}
				placeholder="Type to filter..."
			/>

			{filteredItems.map(item => <div key={item}>{item}</div>)}
		</>
	)
}
```