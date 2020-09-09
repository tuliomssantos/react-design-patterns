#   Switching Component

A switching component is a component that renders one of many components.

Use an object to map prop values to components


```js
const App = () => {
  return (
    <div>
      <Pager page={'about'}/>
    </div>
  )
}
```
```js
const Pager = (props) => {
  const Switcher = pages[props.page] || NotFound;

  return <Switcher {...props} />
}
```

```js
const pages = {
  home: Home,
  about: About,
  user: User
}
```

```js
const Home = () => {
  return(
    <div>
      Home
    </div>
  )
}

const About = () => {
  return(
    <div>
      About
    </div>
  )
}

const User = () => {
  return(
    <div>
      User
    </div>
  )
}

const NotFound = () => {
  return(
    <div>
      NotFound
    </div>
  )
}
```