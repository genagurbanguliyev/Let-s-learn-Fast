> [!info] All state updates are "urgent" by default

`useTransition` - to specify certain updates as non-urgent.(transitions can make apps more responsive)

A great use cases `useTransition` a filtering list:
```js
const [filter, setFilter] = useState("")
const [inputValue, setInputValue ]= useState("")
const [isPending, startTransition] = useTransition()

const filteredItems = items.filter(item => item.includes(filer))

<>
	  <input
	  value={inputValue}
	  onChange={(event) => {
		  setInputValue(event.target.value)
		  startTransition(() =>{
			  setFilter(event.target.value)
		  })
	  }}
	  placeholder="Type to filter..."
	  />
	  {
		  isPending ?
		  <p>Loading...</p>
		  filteredItems.map(item => <div key="item">{item}</div>)
	  }
```


