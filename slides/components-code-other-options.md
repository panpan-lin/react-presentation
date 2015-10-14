```js
var Todo = React.createClass({
  // validate props being passed to your components.
  propTypes: {
    title: React.PropTypes.string.isRequired,
    onDelete: React.PropTypes.func.isRequired
  },
  // Invoked once before the component is mounted.
  // The return value will be used as the initial value of this.state
  getInitialState: function() {
    return {
      checked: false
    };
  },
  handleChange: function() {
    this.setState({checked: !this.state.checked});
  },
  _onDelete: function () {
    this.props.onDelete(this.props.title);
  },
  render: function() {
    var trStyle = this.state.checked ? style.checkedTodo : style.notCheckedTodo;
    return (
      <tr style={trStyle}>
        <td style={style.tableContent}><button onClick={this._onDelete}>X</button></td>
        <td style={style.tableContent}><input type="checkbox" checked={this.state.checked} onChange={this.handleChange} /></td>
        <td style={style.tableContent}>{this.props.title}</td>
        <td style={style.tableContent}>{this.props.children}</td>
      </tr>
    );
  }
});
```
