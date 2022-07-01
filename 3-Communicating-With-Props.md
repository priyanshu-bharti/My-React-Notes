# Communicating With Props

## 3 Tenets of Components

### 1. Nesting

A component can be shown inside of another component.

```js
function App() {
  return (
    <ParentComponent>
      <ChildComponent />
    </ParentComponent>
  );
}
```

### 2. Reusability

We should create components that can be used throughout our application with minimal configuration.

### 3. Configuration

We should be able to change or control the properties of a component upon creation.

## Passing data as props

- We can pass data to any component using the same syntax as we use in HTML attributes.
- Props are the properties that can be passed from a component to the other.
- Props are received as objects that can be received in the formal argument of the functional component.
- A common usecase is to destructure the props object and only use what we really need.

```js
// Here { content } is the prop inside the props object.
export default function CommentText({ content }) {
  return <div className="text">{content}</div>;
}
```

```js
// This is how you pass a props data.
<CommentText content={item.content} />
```

## Passing Children as props

- Sometimes we even need to send children as props to our custom component.
- Props object contain children property that can be used to gain access to the children we pass.

```js
<Block>
  <Avatar url={item.pic} />
</Block>
```

To receive the components we can use `props.children` or destructured `children`

```js
export default function Block({ children }) {
  return <div> {children} </div>;
}
```
