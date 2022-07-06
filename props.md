# Props

---

<br>

### What is it?

Props are arguments passed into react components
Props can be a value, a function, a variable, an array, object or any other datatype
Props are a way to pass these data values from a parent component to a child component

### Advantages

- Instead of exporting and importing data into each component we can pass the values through props which allows the flow of the app to be dynamic

- Props make components more reuseable

---

<br>

### How is it used?

A component receives props as an object in the space for parameters and reads the values for the variable created on the Garage function:

```javascript
function Car(props) {
  return <h2>I am a {props.brand}!</h2>;
}

function Garage() {
  const carName = "Ford";
  return (
    <>
      <h1>Who lives in my garage?</h1>
      <Car brand={carName} />
    </>
  );
}
```

---
