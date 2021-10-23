# Nested components

Nesting components can be very useful as it can behave as the primary building blocks of the React application.

```
import React from "react";
import ReactDom from "react-dom";

const Greeting = () => {
    return (
        <React.Fragment>
            <Person />
            <Message />
        </React.Fragment>
    );
}

const Person = () => {
    return (
        <h1>Aatif</h1>
    );
}

const Message = () => {
    return (
        <h1>How are you ?</h1>
    );
}

ReactDom.render(
    <Greeting />,
    document.getElementByID("root");
);
```

This snippet will create 2 function components & render inside the main component.
