# useContext

---

<br>

### What is it?

useContext is a React hook that makes it easy to pass data throughout your app without manually passing props down the component tree.

![Image of prop drilling](/images/Screenshot%202022-07-06%20at%2011.36.23.png)
![Image of useContext](/images/Screenshot%202022-07-06%20at%2011.36.32.png)

<br>

### Advantages

- You can send data from the top of component tree to any nested components without having to pass the data/props to each level in the component tree first

- this saves lots of time

- you know where the data is at any given point in time so it can be followed

- makes code easier to read

- any time the provider valuechanges that value is reflected across all components that 'use' the 'Context' of that value.

---

<br>

### How is it used?

Step 1:
At the top level of app.js import createContext:

```javascript
import { createContext } from "react";
```

---

<br>

Step 2:
Create a variable using the createContext that you just imported and export it so it can be used anywhere else:

```javascript
export const UserContext = createContext("");
```

---

<br>

Step 3:
Wrap the components that you want to receive data/props in a UserContext.Provider tag and pass the value you want to give to them:

```javascript
<UserContext.Provider value="This is a value being passed to two components">
  <ComponentOne />
  <ComponentTwo />
</UserContext.Provider>
```

---

<br>

Step 4:
Import useContext from react
Import userContext from the file where you created the userContext initially

Example using the value passed:

```javascript
import { useContext } from "react";
import { userContext } from "..App.js";

function ExampleComponent() {
  const value = useContext(userContext);

  return <h1>{value}</h1>;
}
```

This value can be anything, a state, a variable, a function or anything you can generally pass as a prop.

---

<br>

### Links to learn more:

<https://www.youtube.com/watch?v=TNhaISOUy6Q&t=357s>
