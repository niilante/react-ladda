react-ladda
===========

React wrapper for [Ladda buttons](https://github.com/hakimel/Ladda).

Installation
------------

```sh
npm install --save react-ladda
```

Browserify takes care of the rest.

Usage
-----

`LaddaButton` is a component that can be wrapped around any single button:

```js
/** @jsx React.DOM */

React = require('react');
LaddaButton = require('react-ladda');

App = React.createClass({
  displayName: 'App',

  toggle: function() {
    this.setState({active: !this.state.active});
  },

  render: function() {
    return (
      <LaddaButton active={this.state.active}>
        <button onClick={this.toggle}>Click here</button>
      </LaddaButton>
    );
  }
});

React.renderComponent(<App />, document.body);
```

All of the options for ladda buttons are supported:

```js
<LaddaButton
    active={true}
    progress={0.5}
    color="#eee"
    size="xl"
    spinnerSize={30}
    spinnerColor="#ddd">
  <button>Click here</button>
</LaddaButton>
```
