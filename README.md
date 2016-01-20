# React Intro
A short introduction to React.

## What is React?
React is a framework that lets you create reusable UI components.  The state and properties of these components are easily managed and are also easily kept in sync with other components that share similar data.

Many people use React to handle their views in an MVC type application.  Since React is just the UI, it doesn't force you one way or another with your development stack, so it can be easy to use in whatever stack you are using or to implement in an existing project.   

## Why use it?

#### Reusable components
React is all about creating reusable components, and the components are encapsulated so they are easy to test, reuse, nest within each other, and more.  It is very easy to define and manipulate your own components, which can be a big productivity boost.

#### Virtual DOM
React is super efficient and performs very well, due largely to how it manages and uses a virtual DOM rather than updating the browser's actual DOM on the fly.  The virtual DOM is just data rather than rendered content, which lets React easily determine what changed.  It knows what needs to update in the actual DOM beforehand, which avoids costly changes to the actual DOM and updates only what needs to be changed - producing optimal performance.  

#### JSX
Another great feature of React is JSX.  It's a syntax that allows you to mix in HTML with JavaScript.  JSX is not required to use React (you can write plain JavaScript if you want) but using JXS is strongly suggested due to how easy it makes writing components.  See the example below:

 Using JavaScript
```JavaScript
render: function() {
  return React.DOM.a({
    href: 'http://facebook.github.io/react'
  }, 'React');
}

//<a href="http://facebook.github.io/react">React</a>
```

Using JSX
```JavaScript
render: function() {
  return <a href="http://facebook.github.io/react">React</a>;
}

//<a href="http://facebook.github.io/react">React</a>
```

#### One-Way Data Flow

## How do I get started?

#### Additional Resources
