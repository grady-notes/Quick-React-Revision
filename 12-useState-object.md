# useState object

```
import React, { useState } from "react";
import ReactDom from "react-dom";

const UseStateObject = () => {
    const [person, setPerson] = useState({
        name: "Aatif",
        age: 19,
        message: "None",
    });
    const changeMessage = () => {
        setPerson({
            ...person,
            message: "Hello",
        });
    };
    return (
        <React.Fragment>
            <h3>{person.name}</h3>
            <h3>{person.age}</h3>
            <h3>{person.message}</h3>
            <button onClick={changeMessage}>
                Change Message
            </button>
        </React.Fragment>
    );
}
ReactDom.render(
    <UseStateObject />,
    document.getElementById("root");
);
```

The above snippet change the message while preserving the entire array whenever the button is clicked.
