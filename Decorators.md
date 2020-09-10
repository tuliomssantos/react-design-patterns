# Decorators

> In object-oriented programming, the decorator pattern is a design pattern that allows behavior to be added to an individual object, either statically or dynamically, without affecting the behavior of other objects from the same class.

> In simpler words, decorators are syntactic sugar, helping you to keep your code readable, and maintainable, by wrapping the extra, or common functionalities in a separate file altogether, which can be shared across different components/classes.

---

## See the example bellow:

```js
// Button.js
const Button = (props) => {
  const { variant = "primary", children, ...rest } = props;

  return (
    <button className={`button ${variant}`} {...rest}>
      {children}
    </button>
  );
};
```

```js
//  Center.js
import "./Center.css";
const Center = (props) => {
  return <div className="center">{props.children}</div>;
};
```

```css
/* center.css */
.center {
  display: flex;
  justify-content: center;
}
```

Then, we can use these components like this:

```js
import React from "react";
import Button from "./Button";
import Center from "../Center/Center";

export const PrimaryCenterButton = () => (
  <Center>
    <Button variant="primary">Primary</Button>
  </Center>
);
```
