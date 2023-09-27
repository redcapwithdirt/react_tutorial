# definition
React Hooks are functions in React that empower functional components with state and lifecycle features for simpler and cleaner code.


# useState Hook
## **useState Hook - Light Switch:**

*Imagine you have a light switch at home. The `useState` hook would represent the current state of the light – either on or off. You can toggle it by pressing the switch button.*

* ***Counter App with useState:**
	Create a simple counter app where users can increment or decrement a count value. The `useState` hook can be used to manage and update the count state.
	
* ***Todo List with useState and useEffect:**
	Build a todo list application that allows users to add, edit, and delete tasks. Use the `useState` hook to manage the list of tasks and the `useEffect` hook to save tasks to local storage.

* ***Dark Mode Toggle with useState:**
	Implement a dark mode toggle feature in your application. Use the `useState` hook to manage the dark mode state and apply corresponding CSS styles.


Example:

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}
```


# useEffect Hook

## **useEffect Hook - Alarm Clock:**

Think of an alarm clock that rings when it's time to wake up. The `useEffect` hook is like setting the alarm. When the time arrives (an event), the alarm (effect) triggers, and you perform an action, like waking up.

*Certainly! `useEffect` is a React Hook that allows you to perform side effects in your functional components. Side effects are actions that happen in a component that can affect things outside the component, such as data fetching, DOM manipulation, or setting up subscriptions.*

***UseEffect is like a watchman for your component.** You tell it what to watch (dependencies), and when that something changes, it takes a specific action.*

* ***Fetching Data with useEffect:**
	Create a weather app that fetches and displays weather data from an API based on the user's location. Use the `useEffect` hook to make API requests when the component mounts.

Example:

```jsx
import React, { useState, useEffect } from 'react';

function DataFetcher() {
  const [data, setData] = useState([]);

  useEffect(() => {
    // Fetch data and update 'data' state
    fetch('https://api.example.com/data')
      .then((response) => response.json())
      .then((result) => setData(result));
  }, []);

  return (
    <div>
      <ul>
        {data.map((item) => (
          <li key={item.id}>{item.name}</li>
        ))}
      </ul>
    </div>
  );
}
```


# useContext Hook

## **useEffect Hook - Alarm Clock** 
Think of an alarm clock that rings when it's time to wake up. The `useEffect` hook is like setting the alarm. When the time arrives (an event), the alarm (effect) triggers, and you perform an action, like waking up.


