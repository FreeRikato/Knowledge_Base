Source: 
1. https://youtu.be/V9i3cGD-mts?list=PLApy4UwQM3UrZsBTY111R6P4frt6WK-G2
2. https://youtu.be/LOH1l-MP_9k

Understanding what is a State is crucial to learn useState hook.

- State is a data that changes over time with renders in React
- Is it loading, Is there an error or Is there data

1. Import `useState` from 'react'
```JavaScript
import {useState} from 'react'
```
2. Create State variables
```JavaScript
const [count, setCount] = useState(0)
```
-> `count` is the state variable that changes based on a condition (button press)
-> `setCount` is the updater function that takes care of updating the state variable i.e. `count` here.
-> Initialise the value of state variable `count` as 0 with `useState(0)`

3. Logic to update the state variable (button press)
```JavaScript
<button onClick={()=> setCount(count + 1)}> Increment </button>
```
- [>] useState is used to 
  - Manage form input
  - Toggle visibility
  - Dynamic styles
  - Counter
