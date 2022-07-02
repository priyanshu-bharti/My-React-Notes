# Class Based Components

## Difference between Functional and Class Based Components

- We have discussed that a component can be a function or a class.
- In the early days of react, the following was the difference between the functional and class-based components:
  - Functional components were only used to produce the static JSX that wouldn't change.
  - Class based components have lifecycle methods that allows us to perform actions at certain point in time.
  - Class based components also have state that keeps track of some piece of information and update the screen whenever the information changes.
- The react now is different:
  - Even functional components are able to perform actions at different points in time using methods known as hooks.
  - Hooks can provide access to the state and rerender the screen upon changes in information.
- Companies with established projects generally use class based components.
- Companies with newer projects use functional or class based components.


## Creating a Class Based Component

- We need to create a component that extends `React.Component`.
- Then we need to define a `render()` method.
- Inside of the render method we need to return some JSX.

```js
import React from "react";

export default class App extends React.Component {
  render() {
    // Some logic here

    return (
      <div>
        Some Component
      </div>
    );
  }
}

```