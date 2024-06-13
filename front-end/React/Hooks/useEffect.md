Types of Effecst:
1. Event-Based (i.e button click)
2. Render-Based (i.e fetching data)

When NOT to useEffect:
1. use own created function for this...
2. use React-Query or framework (Nextjs) tool

When To useEffect:
1. Ideal for syncing your React code with Browser APIs:
here we were syncronyzing react state with the browser media API using a `ref` (playing or pausing it)
```js
const ref = useRef(null)

useEffect(() => {
	if(isPlaying){
		ref.current.play()
	} else {
		ref.current.pause()
	}
}, [isPlaying])


<video ref={ref} src={src} loop plasInline />
```
