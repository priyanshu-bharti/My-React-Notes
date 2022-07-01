# 1. Diving in

## Some questions about react

### What is React?

- It is a JavaScript Library
- It basically displays some HTML code
- Changes the HTML Code when the user does something.
- Makes the system react to the user's actions.

### How does a React Application Start up?

- We tell react to output some HTML by creating functions that returns some JSX.
- These functions that return JSX are called components.
- JSX looks like HTML tags, but also allows us to directly embed JS code and even create custom components.
- Now, The way the project starts is that React looks at the HTML file and finds the element with the id of root. (It is a div BTW).
- Then it tells react to take control of that element.
- Then it tells react to get the JSX from the app component, turn it into HTML and show it inside the root element (div).

## Setting up the environment

- Install NodeJS
- Create a new project using `npx create-react-app <projectName>` command in the terminal.
- Open the project folder in some IDE and start working.
- To start the application use `npm start` 
- To stop the application press `Control + C` 
- To view the application open `localhost:3000` on your browser.


