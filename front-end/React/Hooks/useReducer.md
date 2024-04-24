`useReducer` use for more complex state management.
GOOD IF: you have a lot of related states
ex:
/                 [ ]
/              /   |   \
/            []   []   []

`reducer` function to update state and can greatly simplify state-related code


GOOD FOR:
###### Anatomy:
```js
const reducer = (state, action) => {
	switch(action){
		case 'increment':                  #4
			return state+1
	}
}

const [count, dispatch] = useReducer(reducer, 0) #1,2

<button onClick={() => dispatch('increment')}>Increment</button> #3
```
 - #1,2:  takes reducer and initial state (0), and returns state (count) and dispatch
 - #3: call reducer with action ('increment')
 - #4: set state conditionally based off the action dispatched


###### Multiple related states:
```js
const reducer = (state, action) => {
	swtich(action.type){
		case 'SET_EMAIL':
			return {...state, email: action.payload}
		case 'SET_PASS':
			return {...state, password: action.payload}
		default:
			return state
	}
}

const initialState = {email: '', password: ''}
const [ state, dispatch ] useReducer(reducer, initialState)

<form>
	<input
		type='email'
		onChange={(e) => {
			dispatch({type: 'SET_EMAIL', payload: e.target.value})
		}}
	/>

	<input
		type="password"
		onChange={(e) => {
			dispatch({type: "SET_PASS", payload: e.target.value})
		}}
</form>
```



###### Depend State: state depends other values
```js
cons gameReducer = (state, action) => {
	switch(action.type){
		case 'move':
			return {...state, position: state.positin + action.distance}
		case 'score':
			return {...state, score: state.score + action.points}
	}
}

const [state, dispatch ] = useReducer(gameReducer, { position: 0, score: 0})

<>
	<p>Position: {state.position}, Score: {state.score}</p>
	<buton onClick={()=>dispatch({type: 'move', distance: 1})}>Move</buton>
	<buton onClick={()=>dispatch({stype: 'score', points:10})}>Score</buton>
</>
```



