# React Router Project

This project covered all the hooks and concepts taught in the Codecademy React Router Module

## Set up

```jsx
import {
  RouterProvider, // Provides React Router to entire application
  createBrowserRouter, // These next two create and initialize a...
  createRoutesFromElements, // ... router object using JSX routes
  Route, // Used to create route objects
} from "react-router-dom";

const appRouter = createBrowserRouter(
  createRoutesFromElements(
    <Route path="/" element={ <Root /> }>
      ...
      ...
      ...
    </Route>
  )
}

function App() {
  return (
    <RouterProvider router={appRouter} />
  );
}
```

`<Root />` - parent component that displays on every page

`<Outlet />` - shows where to  display child components within `<Root />`

`<Route index element={...}/>` - default child route

## Links

`<Link>` creates link for navigation. `<Link to="">` replaces `<a href="">` and will not trigger a page reload.

`<NavLink>` special type of `<Link>` that can be styled differently when the link is active. A function can be passed to `className` or `style` attributes to apply a custom "active" class or style.

`className={ ({ isActive }) => isActive ? 'active-navlink': ''}>`

`isActive` property is destructured and used to apply the `active-navlink` class when `isActive` is true.

## URL Parameters

A URL param looks like `:param` - append a question mark if optional: `:param?`

`<Route path="/books/:bookId/:page?">`

// In progress
