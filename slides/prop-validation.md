###  Prop Validation

<a href="https://facebook.github.io/react/docs/reusable-components.html#prop-validation" target="_blank">Validate</a> that components are passed with all needed properties by:
```propTypes``` and ```React.PropTypes```.
```js
React.createClass({
  propTypes: {
    name: React.PropTypes.string.isRequired,
    id: React.PropTypes.number.isRequired,
    alt: React.PropTypes.string
  },
  /* ... */
);
```
<small>Note that for performance reasons ```propTypes``` is only checked in development mode.</small>
