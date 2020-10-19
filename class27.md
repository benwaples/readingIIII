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

## [Typechecking Props](https://reactjs.org/docs/typechecking-with-proptypes.html)
Typechecking react props is checking the data type being passed each prop. So if a prop should be getting an object it would break if it got an array. Example: 
```js 
import PropTypes from 'prop-types';

class Greeting extends React.Component {
  render() {
    return (
      <h1>Hello, {this.props.name}</h1>
    );
  }
}

// check all prop types here
Greeting.propTypes = {
  name: PropTypes.string
};
```
*  For performance reasons, propTypes is only checked in development mode.

* you can set a default value for a prop value

* you can require certain props are sent to the children


## [Components and Props](https://reactjs.org/docs/components-and-props.html)
> Components let you split the UI into independent and reuseable pieces.
* each component behaves like a function and can take perimeters called props. Each prop holds a value that will then be used by the the child.

## [handling events](https://reactjs.org/docs/handling-events.html)
Much similar to handling events on DOM elements, just slightly different syntax. For example: 
```js
activateLasers = () => {
  turnOnLasers()
}
<button onclick={this.activateLasers()}>
  Activate Lasers
</button>
```

## [snapshot testing](https://jestjs.io/docs/en/snapshot-testing)
Snap shot test are a way to make sure each part of the UI renders how the developer wants. When the UI component loads, the test takes a snapshot and compares it alongside a reference snapshot; the test will fail if the two snapshots are not the same.

### snapshot testing with Jest
``` js
import React from 'react';
import renderer from 'react-test-renderer';
import Link from '../Link.react';

it('renders correctly', () => {
  const tree = renderer
    .create(<Link page="http://www.facebook.com">Facebook</Link>)
    .toJSON();
  expect(tree).toMatchSnapshot();
});
```

First time the test is run, the reference snap shot will be taken, each test there after will be compared to the reference snap shot. 

* if the implementation of the component has changed, so the UI changed, the test will fail. To update the reference snapshot, run `Jest --updateSnapshot'.

## [React Testing Library]()

