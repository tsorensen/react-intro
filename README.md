# React Intro
A short introduction to React - what it is and what features make it worth using.

## What is React?
React is a framework that lets you create reusable UI components.  The state and properties of these components are easily managed and are also easily kept in sync with other components that share similar data.

Many people use React to handle their views in an MVC type application.  Since React is just the UI, it doesn't force you one way or another with your development stack, so it can be easy to use in whatever stack you are using or to implement in an existing project.   

## Why use it?

#### Reusable components
React is all about creating reusable components, and the components are encapsulated so they are easy to test, reuse, nest within each other, and more.  It is very easy to define and manipulate your own components, which can be a big productivity boost.

#### Virtual DOM
React is super efficient and performs very well, due largely to how it manages and uses a virtual DOM rather than updating the browser's actual DOM on the fly.  The virtual DOM is just data rather than rendered content, which lets React easily determine what changed.  It knows what needs to update in the actual DOM beforehand, which avoids costly changes to the actual DOM and updates only what needs to be changed - producing optimal performance.  

#### JSX
Another great feature of React is JSX.  It's a syntax that allows you to mix in HTML with JavaScript.  JSX is not required to use React (you can write plain JavaScript if you want) but using JXS is strongly suggested due to how easy it makes writing components.  See the example below on the difference of writing plain JavaScript vs JSX when outputting a DOM element inside a components render method:

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
In a more traditional MVC framework, different views can communicate data back and forth with each other, which can make it difficult to keep the data in sync as the application grows and becomes more complex.  React is built to use a one-way data flow, which means that the components are immutable and only listen to data coming from upstream in the application rather than each other.  This is why it is easy to keep components in sync with each other - since they are updating from the same, higher source.

When data upstream is updated or changed, the components that are using that data automatically update to reflect those changes.  To use this type of data binding, React uses an application architecture called Flux.  Flux utilizes unidirectional data flow - so when a user interacts with a React view, the view propagates an action through a central dispatcher (a part of Flux) to the different places that house the app's data and business logic, which then updates all views that use that data.  This complements React's declarative programming style very nicely - helping React to refresh only the changed parts when the data is updated.

#### Other advantages
###### SEO
React actually does great with SEO.  A big issue with some JavaScript frameworks is that they are not SEO friendly.  While improvements in this area have been made in recent years, it can still be hard for search engines to read JavaScript-intensive web apps.  React stands out here because you can run React.js on the server - allowing the virtual DOM to be rendered and returned to the browser as a regular web page.

###### Dev Tools
There is an offical React.js [Chrome extension](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi) and [Mozilla add-on](https://addons.mozilla.org/en-US/firefox/addon/react-devtools/) made specifically for developing apps with React.  It not only helps with debugging - it also lets you look directly at the virtual DOM as if you were browsing a regular DOM tree.

###### Maintained by Facebook, growing community
React was first developed internally by Facebook, but it is now open source.  After using it internally for a while, the engineers at Facebook wanted to share what they had created with the world.  There is now a large and growing community of React developers, which is great because it is easy to find free resources, tutorials, help, etc., for getting started.  
## Demo
Short React demo below by Brian Hefter
<p data-height="268" data-theme-id="0" data-slug-hash="gnfew" data-default-tab="result" data-user="bhefter" class='codepen'>See the Pen <a href='http://codepen.io/bhefter/pen/gnfew/'>gnfew</a> by Brian Hefter (<a href='http://codepen.io/bhefter'>@bhefter</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

## How do I get started?
The [React website](https://facebook.github.io/react/index.html) has a great [getting started guide](https://facebook.github.io/react/docs/getting-started.html) and [tutorial](https://facebook.github.io/react/docs/tutorial.html).  They provide you with instructions on how to install it using NPM or by downloading a zipped file with everything you need.  They also provide instruction on how to use [Babel](https://babeljs.io/) as a transpiler if you plan on using ES2015.

Besides this official getting started guide, there are many free, online resources that can help you to quickly get started on using React in your project.

#### Additional Resources
* [React site](https://facebook.github.io/react/index.html)
* [React GitHub](https://github.com/facebook/react)
* [Flux site](https://facebook.github.io/flux/)
* [Babel](https://babeljs.io/)
* [6 Reasons Why We Love React.js](https://www.syncano.io/blog/reactjs-reasons-why-part-1/)
* [Getting Started with React.js](https://www.syncano.io/blog/getting-started-reactjs-tutorial/)
* [An Introduction to React.js](http://www.instrument.com/latest/an-introduction-to-react-js)
