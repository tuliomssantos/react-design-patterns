#   [Higher-order component](https://reactjs.org/docs/higher-order-components.html)

A higher-order function is a function that takes and/or returns a function. It's not more complicated than that.

```js
const Greeting = ({ name }) => {
  if (!name) {
    return <div>Connecting...</div>;
  }

  return <div>Hi {name}!</div>;
};
```