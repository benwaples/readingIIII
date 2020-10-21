# Reading Summary for Class 28

## [Architectural styles and patterns](https://medium.com/@mlbors/architectural-styles-and-architectural-patterns-c240f7df88a0#:~:text=Architectural%20Patterns%20VS%20Design%20Patterns&text=In%20a%20few%20words%2C%20while,and%20mechanisms%20of%20a%20system.)
> The purpose of Architectural Patterns is to understand how the major parts of the system fit together and how messages and data flow through the system.

* architectural patterns are high-level and encompassing of the whole app. Design patterns are of a specific code section.

* architectural styles are different from patterns, the style is the name given to the reoccurring architectural patterns.

> An Idiom is a low-level pattern specific to a programming language.

### layers
Most of the time we have 4 layers:
* Presentation layer or UI layer
* Application layer or Service layer
* Business logic layer or Domain layer
* Data access layer or Persistence layer

MVC is an layered design.

### Event-Driven(EDA)
Designed around the events. Emmitters know the event has happened, a consumer just needs to know an event has occured and it will consume the event. 

* Often used in async operations and UIs.

### Domain Driven Design(DDD)
Software designed after the business domain.
> DDD isn't a way to code but a way to think about things.

### Pipes and Filters
Filters are components that transform the data and change the shape and pipes are the things connecting the components.

Pump produces the data.

Sink consumes the data, or is the final stop for the data.

### Microservice
Mutually exclusive components that come together to make one big application. Opposite of a monolithic architecture that every component depends on each other.

## [Container Presentation Pattern](https://alchemycodelab.github.io/fsjs-notes/05_react/patterns/container_presentation/)
>containers : are stateful components that contain your business login
* manage all of the business logic like hitting APIs, setting up props, munging data, and setting up event handlers.
>presentations : are stateless components that present your data
* receive data through props and render DOM elements

## [Container Details](https://alchemycodelab.github.io/fsjs-notes/05_react/patterns/container_presentation/container-details)
Containers extend reacts Component class. That way it has lifecycle hooks and all the other state managing tools that come with that class.

## [Presentation Details](https://alchemycodelab.github.io/fsjs-notes/05_react/patterns/container_presentation/presentation-details)
Functional components, returning the JSX or TSX from the function.

## [Functional vs Class Components](https://medium.com/@Zwenza/functional-vs-class-components-in-react-231e3fbd7108)
Why use functional components at all:
* Functional components are easier to read and test because they are plain JS.
* less code
* help other developers know which components manage state.
* React says there could performance benefits to functional components down the road.

## [Conditional Rendering](https://reactjs.org/docs/conditional-rendering.html)
Easily have conditional rendering based on user state and input by storing JSX in variables.

Use conditional operators to have react decide what to render for the component.