# Advanced State with Reducers

## Vocabulary Terms
| Term | Definition |
| ---- | ---- |
| State Hook |  It declares a “state variable” letting us add local state to React components. |
| Component Lifecycle | Lifecycle methods are special methods built into React, used to operate on components throughout their duration in the DOM. | 

## Questions

### How can we ensure that an effect hook runs only once?

We can ensure an effect hook only runs once by passing an empty array to it.

```JavaScript
useEffect(() => {
  document.title = `You clicked ${count} times`;
}, []
```

### Can useState() update more than one state variable at the same time?

useState can one state variable at a time, if we store multiple key values pairs in one state object we can update those simultaneously.

```JavaScript
const [state, setState] = useState({});
setState(prevState => {
  // Object.assign would also work
  return {...prevState, ...updatedValues};
});
```

### Is useState() synchronous?

`useState()` and `setState()` both are asynchronous. They do not update the state immediately but have queues that are used to update the state object.

## Sources

[Using the State Hook](https://reactjs.org/docs/hooks-state.html)

[useReducer hook](https://reactjs.org/docs/hooks-reference.html#usereducer)

[Ultimate Guide to useReducer](https://blog.logrocket.com/guide-to-react-usereducer-hook/)

[Using the Effect Hook](https://reactjs.org/docs/hooks-effect.html)

[Provide callback to useState hook like setState](https://www.linkedin.com/pulse/provide-callback-usestate-hook-like-setstate-saransh-kataria/)

[React Lifecycle Methods Diagram](https://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)

[Lifecycle Methods](https://www.theodinproject.com/paths/full-stack-javascript/courses/javascript/lessons/lifecycle-methods)