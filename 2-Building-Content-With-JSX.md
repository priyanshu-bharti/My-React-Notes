# 2. Building Content With JSX

## Creating a React App From Scratch

- We do not need all the files that our react app comes with.
- Instead we just need the index.html file inside the public directory, index.js inside the src directory, and the node_modules folder along with package.json and package_lock.json
- After getting rid of the files, we need to rewrite the index.js file and have it contain the following 5 things
  1. Import the React and ReactDOM libraries
  2. Get a reference to the div with the ID or root
  3. Tell react to take control of the element
  4. Create a component
  5. Render the component on the screen.
- After writing the code, it would look something like this:

```js
// Import the required libraries
import React from "react";
import ReactDOM from "react-dom";

// Get the reference to the root element
const el = document.getElementById("root");

// Take control of the root
const root = ReactDOM.createRoot(el);

// Create a component
function App() {
  return (
    <div>
      <h1>This is a react app</h1>
    </div>
  );
}

// Render the component on the screen
root.render(<App />);
```
