# Web_Dev_Notes

JSX Attributes & Styling React elements: in order to add any css class to html elements we need to make use of keyword “className” instead of “class”. 
Also the attributes name should be in camel case for JSX

Inline Styling for React Elements: 
In order to insert inline css in html in JSX we need to create a css properties as Javascript object and need to use 2 curly braces {{}} as inner curly braces required for JS object and outer one to denote we are embedding JS in html. You can see the implementation below:
ReactDOM.render(
  <h1 style={{ color: "red" }}>Hello World!</h1>,
  document.getElementById("root")
);
Or you can do one thing is to create a javascript object earlier and then insert it into single curly braces.
const customStyle = {
  color: "red"
};

ReactDOM.render(
  <h1 className="heading" style={customStyle}>
    {greetings}
  </h1>,
  document.getElementById("root")
);


React Components:
Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions but work in isolation and return HTML.
Components come in two types, Class components and Function components.
The name of components must be in Pascal case i.e. initial letter must be Capitalized.
Function Components:
A Function component also returns HTML, and behaves much the same way as a Class component, but Function components can be written using much less code, are easier to understand. Below is given a example of function Component.
function Heading(){
return <h1> My Favourite Foods</h1>
}
ReactDOM.render{
<div>
<Heading/> // if we don’t have html children then we can use self closing tag 
<Headi	ng> dsalfa </Heading> //if we have html children then we shall use opening and closing tags of the components.
</div>,
Document.getElementById(“root));

We need to do ES6 import and export of React Components as we can’t define all components  in index.js hence we create different components with .jsx extension.
Also in all components we need to import React initially in order to create components.
For export we need to write “export default <component-name>;” this line shall not include parenthesis() – as it will do direct export and will include that component immediately and can’t be used as component.

Basic Structure of React: 
Initially index.js contains only import of App.jsx component.
App.jsx component is the root component that contains all the imports of rest of components.
Also put all the components including app.jsx in components folder.

JavaScript ES6 – Import, Export and Modules:
JavaScript ES6 Import, Export and Modules helps us to break our large project file into small modules and with the use of Import and Export we can make use of those modules.

Cmds:
Import React from “react” – this will import the React module
Export default <component-name>; - this will do the default export of a function or expression from the module – so whenever you import that module the default function/expression will be imported. You can use any name for the default import.
E.g. Import x from math.js – will give you whatever the default function you have defined in that module.
Export {<name>,<name2>}; - this will do the non-default export of function/expression from the module – and while importing you need to be careful with the names of functions/expressions.
Import * as <name> from math.js: this will import all the functions/expressions from the module. This is discouraged in many coding style.
Import PI, {<name1>,<name2>}: this will import the default as PI and other 2 names will also be imported.

Done till lecture_315
