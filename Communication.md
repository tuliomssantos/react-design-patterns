#  [Communication](https://github.com/krasimir/react-in-patterns/blob/master/book/chapter-02/README.md#input)
![Communication](/communication.jpg)

*   Every React component is like a small system that operates on its own. It has its own state, input and output. In the following section we will explore these characteristics.
*   React is not defining strictly what should be passed as a prop. It may be whatever we want. It could even be another component.

---
## Input

```jsx
// Title.jsx
function Title({ text }) {
  return <h1>{ text }</h1>;
}

// App.jsx
function App() {
  return <Title text='Hello React' />;
}
```

---
## Output
*   The first obvious output of a React component is the rendered HTML. Visually that is what we get. However, because the prop may be everything including a function we could also send out data or trigger a process.

```jsx
const NameField = ({ handleNameChange }) => {
  return (
    <input
    onChange={(e) => {handleNameChange(e.target.value)}} 
    />
  );
};
```

```jsx
const App = () => {
  const [name, setName] = useState('');
  const handleNameChange = (updatedName) => {
    setName(updatedName)
  }
  return (
    <div>
      <h1>Name: {name}</h1>
      <NameField handleNameChange={handleNameChange} />
    </div>
  )
}
```