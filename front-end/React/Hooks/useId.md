`useId()` - creates unique ids. its usefull when form input reuse multiple times in a single page.

ex:
```js
functin Form(){
	return(
		<form>
			<EmailInput name="Email"/>
			<EmailInput name="Confirm Email" />
		</form>
	)
}


#########################################
function EmailInput({ name }){
	const id = useId()

	return(
		<>
			<label htmlFor={id}>{name}</label>
			<input id={id} type="email" />
		</>
	)
}

```