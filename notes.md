# ReactJS Notes

**1. Components and Web Components:** Piece of a framework that encapsulates something. It can be an object or a view or anything like that. It is an encapsuated pieace that can be used at multiple places in the app.

[Web Component](https://www.webcomponents.org/)

**Advantages** Reuse code, embedd these components together and can be used at mlltiple places.

Comparing React components with MVC architecture. React is only the view component of a MVC framework.

React can be embedded with angular. Only the the view portion will be react.
React can also be used to design a webpage in react way by combing it with `state` management library like `Redux` to build the app.

**2. React Components:** React is not necessarily a MVC. It can be used as an MVC but not a necessity. React components are different from web components or components in other languages.

A simple react component :
```
  /*Creating a react component */
  Var MsgComponent = React.createClass({
    render: function() {
      return (
        <div>{this.props.message}</div>
      );
    }
  });

  /*Rendering an instance of msgComponent on the document body */
  ReactDOM.render (
    <MsgComponent message="Hello!" />,
    document.body
  );
```

To create a react component. `React.createClass` function is used a an object is passed as a parameter. In this object `states` can be maniplated.

Render is the only function that is required. Render function will contain the jsx that is written. Jsx is syntax extension of js. Elements that a component should contain should be written in render function.

**Props:** These are properties that are passed into a component. Like `message="Hello!"`.

**this:** `this` is the component itself. Like `MsgComponent`.

**3. JSX:** A way to write html in javascript. It is not exactly html. JSX can't be sent to the browser directly. It should always be transpiled using `bable.js` or similar transpilers. JSX is just for developers convinience. Bable converts JSX into react function that converts JSX into elements and that is sent to the browser. JSX can't be directly sent to the browser. What is sent to browser are react functions that are created used transpilers. If we look at the code above the return function in the render method is converted to javascript even though it is html. And thats why we can use `this` and other javascript inside html.

React components can be rendered on `ReactDOM`. It can also be rendered on other systems as well.

**ReactDOM:** ReactDOM is a glue between react and DOM. Any react components are rendered through reactDOM. Some main function of reactDOM are 1) `reactDOM.render()` - to render components and 2) `ReactDOM.findDOMNode()` - to find or get direct access to elements on the DOM.

The above methods are the only things that are required to create a react component.

**Introduction to React Components**
