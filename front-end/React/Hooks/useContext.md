`useContext` - works in any component thats nested inside a provider, no matter how deep it is. To read the context value your just need pass the created context to use context and thats it.

ex:
```js
const ThemeContext = createContext()

funtction App(){
	return(
		<ThemeContext.Provider value="dark">
			<Form />
		</ThemeContext.Provider>
	)
}

#######################3
function Form(){
	const theme = useContext(ThemeContext)
}
```