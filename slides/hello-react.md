### Hello React
(jsx)

```js
var Hello = React.createClass({
  render: function() {
    return <div>Hello {this.props.name}</div>;
  }
});

React.render(<Hello name='React' />, document.getElementById('container'));
```
