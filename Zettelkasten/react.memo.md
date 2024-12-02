- prevents a component from re-rendering if its props haven't changes, which can improve the performance of React applications
- especially for components that are expensive to render or are rendered frequently

=> compares previous props with new props
=> if same, react skip rendering the component and reuse last rendered output
=> else re-renders


### Example:
```jsx
function App() {
  const [count, setCount] = useState(0);
  const [text, setText] = useState('');

  return (
    <div>
      <h1>Count: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Increment Count</button>
      <input
        type="text"
        value={text}
        onChange={(e) => setText(e.target.value)}
        placeholder="Type something..."
      />
      <MemoizedExpensiveComponent title="Expensive Component" />
    </div>
  );
}

const ExpensiveComponent = ({ title }) => {
  console.log('Expensive component rendered!');
  return <div>{title} is expensive to render.</div>;
};

const MemoizedExpensiveComponent = React.memo(ExpensiveComponent);
```

- `React.memo` checks if title prop has changed when the parent component (App) re-renders
- If the title prop stays the same between renders, then `ExpensiveComponent` won't re-render
