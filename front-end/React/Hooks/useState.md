`useState` use for that you need simple state ||state value that contains little data in it


```js
const [age, setAge] = useState(18)
```
 - `18` : set initial value
 - `age` : put value in this variable
 - `setAge` : functions to update variable (`age`)
 - `[age,setAge]` : destructure returns array

examples
###### `useState` : manage form input
```js
const [value, setValue] = useState("")

const handleChange = (e) => {
	setValue(e.target.value)
}

<input
	type="text"
	value={value}
	onChange={handleChange}
```


###### `useState` : toggle visibility
```js
const [isVisible, setVisible] = usestate(false)

# Click to show or hide element
<button onClick={() => setVisible(!visible)}>
Toggle
</button>

{isVisible && <div>Content to Show/Hide</div>}
```


###### dynamic styles
```js
const [isActive, setIsActive] = useState(false)

<button className={isActive ? 'active' : 'inactive'}
		onClick={() => setIsActive(!isActive)}>
	Click
</button>


```