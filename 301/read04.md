# Forms 
Just like in HTML, React uses forms to allow users to interact with the web page.

### Example:
Add a form that allows users to enter their name:
```
class MyForm extends React.Component {
  render() {
    return (
      <form>
        <h1>Hello</h1>
        <p>Enter your name:</p>
        <input
          type="text"
        />
      </form>
    );
  }
}
ReactDOM.render(<MyForm />, document.getElementById('root'));
```

## Controlled Components
In HTML, form elements such as ```<input>```, ```<textarea>```, and ```<select>``` typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with ```setState()```.

### Example:
```
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

# The Conditional (Ternary) Operator Explained

The conditional (ternary) operator is the only JavaScript operator that takes three operands```:``` a condition followed by a question mark (```?```), then an expression to execute if the condition is truthy followed by a colon (```:```), and finally the expression to execute if the condition is falsy. This operator is frequently used as a shortcut for the if statement.

### Example
```
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
 }
  ```
### Result
```
x==y ? console.log(true) : console.log(false)
```