# 6. Life Cycle Methods

## What are lifecycle methods?

- They're special methods that are defined in the React.Component class and are available in all our stateful components.
- They allow us to execute code at certain points in time.
- Some of the lifecycle methodss are:
  1. **`Constructor`** : Good for doing intital setup
  2. **`Render`** : Avoid doing anything besides returning JSX
  3. **`ComponentDidMount`** : Good place to load data.
  4. **`ComponentDidUpdate`** : Good place to load data when the state changes.
  5. **`ComponentWillUnmount`** : Used when performing certain operations for cleanup (usually non-react stuff).

## Why use Lifecycle methods?

- We can use either constructor or componentDidMount to load data but it is recommended to use `componentDidMount()`
- Also ComponentDidMount makes it easy to understand that we are trying specifically to load some data.