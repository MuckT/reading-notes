# 401 Component Lifecycle / useEffect()

## Vocabulary Terms
| Term | Definition |
| ---- | ---- |
| State Hook | A Hook is a special function that lets you “hook into” React features; useState is a Hook that lets you add React state to function components. |
| Mounting and Un-Mounting | Mounting and un-mounting are synonyms with setup and cleanup. With functional components this can be displayed as follows. 
```
import React, { useEffect } from 'react';
const ComponentExample => () => {
    useEffect(() => {
        // Anything in here is fired on component mount.
        return () => {
            // Anything in here is fired on component unmount.
        }
    }, [])
}
```

## Questions

### Why do we not need more .html pages in a multi-page React app?

A React app consists of a single HTML file index.html separate pages or components are contained within `.js` files that contain `.jsx`. If we want the experience of multiple papges, we would create additional components and possibly some top level navigation such as [BrowserRouter](https://v5.reactrouter.com/web/api/BrowserRouter) or [ReactNavigation](https://reactnavigation.org/docs/getting-started).

### If we wanted a component to show up on every page, where would we put it and why?
- Option 1: Outside the <BrowserRouter/>
- Option 2: Inside the <BrowserRouter />, outside a <Route />
- Option 3: Inside a <Route />

Option 2 would be the correct choice. We want the component to be inside of BrowserRouter which commonly wraps app; however, we don't want it inside of a route as this would conditionally render based on the path.

### What does routing do with the components that were rendered when a new route is requested?

The components rendered are updated based on the new route and the history object is updated.

### What does props.children contain?

The child prop is returned for all paths irrespective of whether the current location matches the path or not.

### How do useState() and this.setState() differ?

`useState()` is used to set state in functional components and `this.setState()` is used to set state in class based components.

## Sources

[Effects Hook](https://reactjs.org/docs/hooks-effect.html)

[BrowserRouter](https://v5.reactrouter.com/web/api/BrowserRouter)

[ReactNavigation](https://reactnavigation.org/docs/getting-started)

[Understanding The Fundamentals of Routing in React
](https://medium.com/the-andela-way/understanding-the-fundamentals-of-routing-in-react-b29f806b157e)