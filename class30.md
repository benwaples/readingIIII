# Reading Summary for Class 30

## [Hooks API](https://reactjs.org/docs/hooks-overview.html)

* hooks are a way to use class componenet features inside of a function component.

`useState()` will return a pair - [state, changeState] - they can be named whatever is relevent. The first position in the pair is what is in state, and the second position is the function to change that specific state.

`useEffect()` is a way to execute a function at the beginning, middle, or end of a component rendering. This acts like a `componentDidMount()` lifecycle hook in a class component. 
 - if you pass `useEffect()` an arrow function, the arrow function will execute after the component mounted. 

## [State Hooks](https://reactjs.org/docs/hooks-state.html)

more on `useState()`

to access state in a class component you would have to do something like this: 
```js
<p>You clicked {this.state.count} times</p>
```
however in a class component, once the pair of values are deconstructed off of `useState()`, they can be used directly. 
```js
const [animal, useAnimal] = useState()

<label htmlFor="animal">Whats your Favorite Animal
<input type="text" name="animal" onChange={() => useAnimal(value)}>
```
## [Effect Hooks]()
## [Hooks API reference]()