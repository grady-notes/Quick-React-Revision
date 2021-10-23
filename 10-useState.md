# useState

useState is a very useful hook in react which returns an array of two values out of which the first one is the initial state that we will define and the other value is a function. This function will control the initial value or the state in other words. While invoking a useState function it is mandatory to pass a default argument. This value can be a string, a number, an array, an object or any valid Javascript data type.

## Rules to use hooks in React.

- Hook name has to start with the word "use"
- Component name must be uppercase
- Hooks cannot be used at the top level, they must be inside a component or a function.
- Hook functions cannot be called in conditions or loops.

```
import React, { useState } from "react";
import ReactDom from "react-dom";

const UseStateBasics = () => {
    const [text, setText] = useState("Hey !");
    const handleClick = () => {
        if (text === "Hey !") {
            setText("Changed");
        } else {
            setText("Hey !");
        }
    };
    return (
        <React.Fragment>
            <h3>{text}</h3>
            <button onClick={handleClick}>
                Click Me
            </button>
        </React.Fragment>
    );
}

ReactDom.render(
    <UseStateBasics />,
    document.getElementById("root");
);
```

The above snippet will keep toggling the text from "Hey !" to "Changed" and vice-versa whenever the button is clicked.
