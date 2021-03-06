# React Learner 2021

My personal React Learner note

## Table of Contents

<!-- !toc (minlevel=2 omit="Table of Contents") -->

* [React's Basic Concepts](#reacts-basic-concepts)
  * [React Components](#react-components)
  * [JSX is NOT HTML](#jsx-is-not-html)

<!-- toc! -->

## React's Basic Concepts
- Components
  - Like Functions
  - Input: props, state | Output: UI
  - Reusable and composable
  - `<Component />`
  - Can manage a private stae
- Reactive updates
  - React will react
  - Take updates to the browser
- Virtual views in memory
  - Generate HTML using JavaScript
  - No HTML template language
  - Tree reconcilition

### React Components
Function Component
```javascript
Props ==>
const MyComponent = (props) => {
  return (
    <domElementOrComponent .../>
  );
}
==> DOM
```
Class Component
```javascript
State ==>
class MyComponent extends React.Component {
  render () {
    return (
      <domElementOrComponent .../>
    )
  }
}
==> DOM
```

### JSX is NOT HTML
```javascript
class Hello extends React.Component {
  render () {
    return (
      <div className="container">
        <h1>Getting Started</h1>
      </div>
    )
  }
}
ReactDOM.render(<Hello/>, mountNode);
```
```javascript
class Hello extends React.Component {
  render () {
    return (
      React.createElement("div", { className: "container" },
        React.createElement("h1", null, "Getting Started")
      )
    );
  }
}
ReactDOM.render(React.createElement(Hello, null), mountNode);
```
