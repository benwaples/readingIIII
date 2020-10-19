# Reading Summary for Class 27

## [setState explained](https://css-tricks.com/understanding-react-setstate/)
> react components with state render UI based on that state
* when the state of the component changes, so does the UI.

>setState() is the only legitimate way to update state after the initial state setup

```js
state = {
  isLoggedIn: false
}

// check to see if user is logged in before loading the whole component
componentDidMount = () => {
  checkCookie() ? setState =({isLoggedIn: true}) : setState =({isLoggedIn: false})
}
```

* you can pass setState() an arrow function that 
* updaters (passing set state an arrow function and returning what you want state to do.)

## [List and Keys](https://reactjs.org/docs/lists-and-keys.html)
* use `map()` to go through an array and dynamically render JSX
* Make sure to give each component a unique `key` to be 'help React identify which items have changed, are added, or are removed'

## [Typechecking Props]()


## [handling events]()


## [snapshot testing]()


## [React Testing Library]()

