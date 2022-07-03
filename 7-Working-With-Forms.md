# 7. Working With Forms

## Controlled vs Uncontrolled Elements

- We never want to store the data inside the HTML element itself.
- We need that data to reside inside the react component.
- Thus we need to store the piece of data as a state and then change the data whenever the input changes.
- This causes the component to rerender and the information to be updated.

## Fixing Cannot read properties of undefined

- If we want to call a method when any event occurs, and we want to invoke any method for handling that event, we must use an arrow function for the invocation
- In practice, it should look something like this.

```js
import React, { Component } from "react";

export default class Example extends Component {
  state = { term: "" };

  onFormSubmit(e) {
    e.preventDefault(); // Prevent the page from refreshing
    // Do something interesting
  }

  render() {
    return (
      // Notice that we need to pass event as a parameter to the function.
      <form onSubmit={(e) => this.onFormSubmit(e)}>
        <div>
          <label>Image Search</label>
          <input
            type="text"
            value={this.state.term}
            onChange={(e) => this.setState({ term: e.target.value })}
          />
        </div>
      </form>
    );
  }
}
```
