
Setting up a React Project on your Mac:

First, you need a server:
For Basic Setup:
Use Live Server in VS Code, right click in file and choose Start Live Server

-- Very Basic Starter HTML File --
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>First Component</title>
</head>
<body>
  <div id="root"></div>
  <script src="https://unpkg.com/react/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom/umd/react-dom.development.js"></script>

  <script src="https://unpkg.com/babel-standalone"></script>
  <script src="App.js" type="text/jsx"></script>

</script>
</body>
</html>
```

--- A Very Basic Class Componenet ---
```jsx
class Hello extends React.Component{
  render() {
    return (
      <h1>Hello from a Class Component!</h1>
    )
  }
}

ReactDOM.render(<Hello />, root)
```

--- And a Very Basic Function Componenet ---
```jsx
function Hello() {
  return (
    <h1>Hello from a Function Component!</h1>
  )
}

ReactDOM.render(<Hello />, root)
```

About JSX:
- Babel transpiles the jsx into valid javascript, which is why it needs to be included as a tool if you wish to use jsx.
- jsx tags must be closed
