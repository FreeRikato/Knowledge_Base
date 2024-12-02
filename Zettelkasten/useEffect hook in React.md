Source: 
1. https://youtu.be/V9i3cGD-mts?list=PLApy4UwQM3UrZsBTY111R6P4frt6WK-G2
2. https://youtu.be/LOH1l-MP_9k

useEffect is used to manage side effects

When something happens/updates/triggers in our application there are side effects or consequences bound to happen.

This mostly happens when there is change in state of the application

> Let's assume a stateful react application
```JavaScript
const [count, setCount] = useState(0)
return <button onClick = {() => setCount(count + 1)}> Increment </button>
```

1. Import `useEffect` from 'react'
```JavaScript
import {useEffect} from 'react'
```
2. Basic structure of the `useEffect` hook
```JavaScript
useEffect(()=>{
  // Code to execute as side effect
  console.log(count)
  // Optional return function
},[count]) // Dependency array
```
- `Effect function`: primary function inside the hook where you put the code that should run as a side effect. Runs after initial render and after every update where the dependencies change.
- `Cleanup function`: optional function to return. Runs before the components unmounts or before the effect is re-run due to change in dependencies. 
> Cleanup functions are useful in cleaning up resources like timers, subscriptions, or any other side effects that need to be disposed of.
- `Dependency array`: array of dependencies that determines when the effect should re-run. If empty then runs only once after initial render and not on subsequent updates else runs after initial render and any time variables change


What happens when a fetch call is done directly in a component?
- This would cause it to run on every render, leading to an infinite loop.

Let's take an example here,
```JavaScript
const MyComponent = () => {
  const [data, setData] = React.useState(null);

  // Fetch is called directly during rendering
  fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => setData(data));

  return (
    <div>
      {data ? <p>{data.title}</p> : <p>Loading...</p>}
    </div>
  );
};
```

1. React first renders 'MyComponent'
2. fetch call is immediately executed and data is returned on network request
3. state variable 'data' is updated with setData after the fetch call
4. state update causes re-render
5. re-render causes 'fetch' to run again
6. Infinite loop
