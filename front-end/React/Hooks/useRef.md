Store Value

`refs` = mutable (can modify directly)
vs
`state` = immutable (can't modify directly)

###### Timer examle:
```js
const [timer, setTimer] = useState(0)
const intervalRef = useRef()

const startTimer = () => {
	intervalRef.current = setInterval(() => {
		setTimer((prevTimer) => prevTimer+1)
	}, 1000)
}

const stopTimer = () => {
	clearInterval(intervalRef.current)
}

<p>{timer}</p>
<buttin onClick={startTimer}>start</button>
<buttin onClick={stopTimer}>stop</button>
```

###### Access DOM Element
```js
const inputEl = useRef(null)
const handleFocus = () => {
	inputEl.curent.focus()
}

<>
	<input ref={inputEl} type="text" />
	<button onClick={handleFocus}>Focus</button>
</>
```