# useEffect - 2nd Parameter

```
import React, { useState, useEffect } from "react";
import ReactDom from "react-dom";

const App = () => {
    const [value, setValue] = useState(0);
    useEffect(() => {
        if (value >= 1) {
            document.title = `New : ${value}`;
        }
    }, [value]);
    return (
        <React.Fragment>
            <h1>{value}</h1>
            <button onClick={() => {
                setValue(value + 1);
            }}>Click Me !</button>
        </React.Fragment>
    );
}

ReactDom.render(
    <App />,
    document.getElementById("root");
);
```

This snippet will change the window title only and only if the {value} shows any change in it becasue the {value} is put inside the list of dependancies. This means that the functioning of the useEffect is depended on the {value}.

The 2nd parameter is the most important part of the useEffect. Every useEffect call must have a list of dependancies or the 2nd parameter. It can contain any desired value or even can be left blank : []
