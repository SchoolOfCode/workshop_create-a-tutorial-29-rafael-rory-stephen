# useContext

---

<br>

### What is it?

useState is one of the most important hooks that allows you to track changes to state.

State usually refers to  data that need to be tracked in the app.

state refers to the reactive data and setState refers to the setter data.

<br>

### Advantages

- Everytime the reactive data changes, React will rerender so that the UI has the latest version.

- These changes can be made on a component level, rather than having to change the whole appilcation.

- This makes it easier to track and easier to read.

---

<br>

### How is it used?

Step 1:
At the top level of app.js import useState:

```javascript
import { useState } from "react";
```

---

<br>

Step 2:
Create a variable using the useState, that returns two values that you can use in your component: [state, setState] and can be used as props.


```javascript
 const [state, setState] = useState(0);
```
This is usually within a function, as shown in step 3. 

The initial state in our example is 0 but this can be anything.

---

<br>

Step 3:
Import useState from react

Example using the value passed:

```javascript
import { useState } from "react";


function ExampleComponent() {
  const [state, setState] = useState(0);

  return ( 
  <> 
    <button onClick={() => setState(state + 1)} >Click to Add 1</button>;
    <p>{state}<p>
  </>)
}
```

Once the button is clicked the state will be changed so the count increases by one, also the the text inside the button will update to reflect the change in state.
---

<br>

### Links to learn more:

<https://beta.reactjs.org/apis/usestate>
