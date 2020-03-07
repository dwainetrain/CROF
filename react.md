
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

ReactDOM.render(<Hello />, document.getElementById('root'))
```

--- And a Very Basic Function Componenet ---
```jsx
function Hello() {
  return (
    <h1>Hello from a Function Component!</h1>
  )
}

ReactDOM.render(<Hello />, document.getElementById('root'))
```
-- Setting Up Your Dev Environment on a Mac --
Easiest way - Create React App (CRA)
Install Node
npx create-react-app <app-name>

About JSX:
- Babel transpiles the jsx into valid javascript, which is why it needs to be included as a tool if you wish to use jsx.
- jsx tags must be closed
- Conditional rendering in jsx: https://blog.logrocket.com/conditional-rendering-in-react-c6b0e5af381e/

-- Common List Pattern --
```jsx
class Hello extends React.Component{
  render() {
    let {to, from, favorite_foods} = this.props
    return (
      <div>
        <h1>Hello, to {to} from {from}!</h1>
        <ul>
          {favorite_foods.map(item => <li>{item}</li>)}
        </ul>
      </div>
    )
  }
}

class App extends React.Component {
  render() {
    return (
      <div>
      <Hello to="Paul" from="Ringo" favorite_foods={["pizza", "cake", "Edamame"]}/>
      <Hello to="Chic" from="Correa" favorite_foods={["rice", "beans", "chicpeas"]}/>
      </div>
    )
  }
}

ReactDOM.render(<App />, root)
```
