# useEffect - Cleanup Function

```
import React, { useState, useEffect } from "react";
import ReactDom from "react-dom";

const Cleanup = () => {
    const [size, setSize] = useState(window.innerWidth);
    const checkSize = () => {
        setSize(window.innerWidth);
    }
    useEffect(() => {
        window.addEventListener('resize', checkSize});
        return () => {
            window.removeEventListener('click', checkSize);
        };
    });
    return (
        <React.Fragment>
            <h1>{size}</h1>
        </React.Fragment>
    );
}

ReactDom.render(
    <Cleanup />,
    document.getElementById("root");
);
```

This snippet will add an event-listener on the window and then remove it when the purpose of the event-listener has been served.
