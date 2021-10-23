# Simple list rendering using map()

The map function destructure the original array into seperate elements and renders them as seperate elements by wrapping then around another HTML element. This new wrapper element is decided by the programmer.

```
import React from "react";
import ReactDom from "react-dom";

const names = ['John', 'Jacob', 'Jingleheimer'];
const newNames = names.map((name) => {
    return (
        <h1>{name}</h1>
    );
});

const NameList = () => {
    return (
        <h1>{newNames}</h1>
    );
}

ReactDom.render(
    <NameList />,
    document.getElementById("root");
);
```

Above snippet will render each of the names in the names array.
