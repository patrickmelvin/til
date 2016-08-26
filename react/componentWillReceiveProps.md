You can use `componentWillReceiveProps` to change the state of a component when it receives new props.

`componentWillReceiveProps` is called before the component is rendered. There is no default check that any of the props have changed.

```
componentWillReceiveProps: (nextProps) => {
  if(nextProps.foo !== this.props.foo) {
    this.setState({
      bar: nextProps.foo > this.props.foo
    });
  }
}
```
