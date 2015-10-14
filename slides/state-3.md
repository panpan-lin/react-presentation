```js
var TodoList = React.createClass({
  getInitialState: function() {
    return {
      data: this.props.data,
      titleValue: "",
      detailValue: ""
    };
  },
  changeTitle: function(e) {
    this.setState({
      titleValue: e.target.value
    });
  },
  changeDetail: function(e) {
    this.setState({
      detailValue: e.target.value
    });
  },
  addTodo: function() {
    var newData = this.state.data;
    newData.push({
      title: this.state.titleValue,
      detail: this.state.detailValue
    });
    this.setState({
      data: newData,
      titleValue: "",
      detailValue: ""
    });
  },
```
