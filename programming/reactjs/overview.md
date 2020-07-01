= react =
Created by Jordan Walke (Facebook), 2011
React is a library that’s designed to update the browser DOM for us.


- React is Declarative (using JSX, it abstracts away the details of how the DOM is to be rendered)



== React ==
- React is the library for creating views.
- The browser DOM is made up of DOM elements.
- React DOM is made up of React elements.
- A React element is a description of what the actual DOM element should look like.

const h1 = React.createElement("h1", { id: "recipe-0" }, "Baked Salmon");

const ul = React.createElement(
  "ul",
  { className: "ingredients" },
  items.map((ingredient, i) =>
    React.createElement("li", { key: i }, ingredient)
  )
);

== ReactDOM ==
- ReactDOM is the library used to actually render the UI in the browser.

ReactDOM.render(h1, document.getElementById("root"));


= React Components =
A user interface is made up of parts. In React, we describe each of these parts as a component.
- components render trees of elements and other components

function IngredientsList({ items }) {
  return React.createElement(
    "ul",
    { className: "ingredients" },
    items.map((ingredient, i) =>
      React.createElement("li", { key: i }, ingredient)
    )
  );
}

- older syntax using fucitons
React.createClass({ render() { })

- older syntax using class
class ComponentName extends React.Component {
  render() {
  }
}


= JSX =
JSX: tag-based Javascript syntax, allows us to define React elements using a tag-based syntax directly within our JavaScript code
- element’s type is specified with a tag
- tag’s attributes represent the properties
- element’s children can be added between the opening and closing tags

React Element: React.createElement(IngredientsList, {list:[...]});
JSX:           <IngredientsList list={[...]} />

Component properties will take two types:
1. either a string or
2. a JavaScript expression. JavaScript expressions can include arrays, objects, and even functions. In order to include them, you must surround them in curly braces.

- Nested Components
<IngredientsList>
  <Ingredient />
  <Ingredient />
  <Ingredient />
</IngredientsList>

- Css Class
<h1 className="fancy">Baked Salmon</h1>

- Expressions, Evaluation
<h1>{title}</h1>
<input type="checkbox" defaultChecked={false} />
<h1>{"Hello" + title}</h1>
<h1>{title.toLowerCase().replace}</h1>

- Mapping Arrays with JSX
<ul>
  {props.ingredients.map((ingredient, i) => (
    <li key="{i}">{ingredient}</li>
  ))}
</ul>

# JSX must be converted into createElement calls using Babel:





https://github.com/brillout/awesome-react-components

npm packages:
1) babel-loader : allows Webpack to load and run babel
2) babel-preset-es2015: to convert ES6 to ES5
  can use babel-preset-env for es2015+ transformations
3) babel-cli and babel-preset-react: to convert JSX to JS
4) babel-cli : Babel CLI (gets installed to node_modeles/.bin/babel)
eg.
  babel src -d lib


= sources =
https://reactjs.org/blog
https://www.robinwieruch.de/react-eslint-webpack-babel/
http://typescript-react-primer.loyc.net/tutorial-5.html
