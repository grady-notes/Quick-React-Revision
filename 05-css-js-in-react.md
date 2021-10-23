# Using CSS and Js in React

```
import React from "react";
import ReactDom from "react-dom";

const Book = () => {
    const title = "Harry Potter";
    const style = {
        color: "red",
        fontSize: "2em",
    };
    return (
        <h1>{title}</h1>
        <p style={style}>
            Written by J.K Rowling
        </p>
    );
}

ReactDom.render(
    <Book />,
    document.getElementByID("root");
);
```

In order to use Javascript in JSX, we have to define a pair of curly braces and in order to use CSS in JSX an object has to be created.

The above snippet will replace the {title} with "Harry Potter" and "Written by J.K Rowling" would be rendered in red color and with an increased font size as give in the style object.
