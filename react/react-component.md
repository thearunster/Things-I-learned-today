# React Components

React allows developers to decompose a complex web UI into a set of compact, reusable, stateless units called Components. React components do not hold state and should be simply used to display the UI. They can be mixed together and nested to create complex user interfaces.

There are two ways of creating a React component, using a function or by using a class:

## Functional component

```js
const myDiv = () => { 
                      return (
                          <div>Hello World!</div>
                        ); 
                    };
```

## Class component

```js
class myDiv extends React.Component {
    constructor(props) {
      super(props);
    }
    
    render() {
      return (
        <div>Hello World!</div>
      );
    }
}
