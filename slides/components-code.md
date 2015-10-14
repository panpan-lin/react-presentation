```js
var TodoBox = React.createClass({
  render: function() {
    return (
      <div className = "todoBox">
        <h1>Todos</h1>
        <TodoList />
        <TodoForm />
      </div>
    );
  }
});

var TodoList = React.createClass({
  render: function() {
    // return some HTML
  }
});

var TodoForm = React.createClass({
  render: function() {
    // return some HTML
});
```
