# Handling the state

## Rules of the state system in React

- States are accessible inside the class based components (by Default) and functional components (only using hooks)
- Props and states can be confusing
- State is a JS object that contains data relevant to the component
- Updating the state causes the component to rerender.
- State must be intialized when a component is created.
- State must be initialized when the component is created. (inside the `constructor()`)
- State can only be updated when `setState()` is called.

## Simple example to initialize, and use state inside class based components.

```js
import React from "react";

export default class App extends React.Component {
  constructor(props) {
    super(props);

    // intialize the state
    this.state = {
      hemisphere: '',
    };
  }

  render() {
    window.navigator.geolocation.getCurrentPosition(
      (res) => {
        if (res.coords.latitude >= 0) {
          this.setState({hemisphere: "northern"})
        } else {
          this.setState({hemisphere: "southern"})
        }
      }),
      (err) => console.log(err)
    );

    return (
      <div>
        <h1>Latitude: {this.state.hemisphere}</h1>
      </div>
    );
  }
}
```
