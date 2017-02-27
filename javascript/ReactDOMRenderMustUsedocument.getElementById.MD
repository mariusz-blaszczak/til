# `ReactDOM.render(component, ...)` DOM element must be `document.getElementById("root")`

Otherwise it raises: `Uncaught Error: _registerComponent(...): Target container is not a DOM element.`

So use this:
```JSX
ReactDOM.render(
  <Counter />,
  document.getElementById("root")
)
```
