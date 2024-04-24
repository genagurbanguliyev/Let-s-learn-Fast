
useEffect                                       vs                      UseLayoutEffect
 - for most side effects               |      - more limited
 - runs after paint                        |      - runs before paint
 - asynchronous                          |      - synchronous


###### useLayoutEffect: Set initial state:
```js
const ref useRef(null)
const [tooltipHeight, setTooltilHeight ] = useState(0)

useLayoutEffect(() => {
	const {height} = ref.current.getBoundingClientRect()
	setTooltipHeight(height)
}, [])
```


