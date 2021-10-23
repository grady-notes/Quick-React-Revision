# Props

Props simply mean properties which can be passed to the function as an argument and as an attribute to a component.

```
import React from "react";
import ReactDom from "react-dom";

const BookList = () => {
    return (
        <Book
            title="Time Machine"
            author="H.G Wells"
        />
    );
}

const Book = (props) => {
    return (
        <React.Fragment>
            <h1>{props.title}</h1>
            <h3>{props.author}</h3>
        </React.Fragment>
    );
}

ReactDom.render(
    <BookList />,
    document.getElementByID("root");
);
```
