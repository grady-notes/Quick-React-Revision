# Custom Hooks

Creating cusotm hooks comes into practice when we have re-usable code and a same function that has to be used in multiple components with separate arguments.

In this module we would be creating a hook which will fetch various API responses and return relevant data. In this module, this hook will be called as useFetch.

```
import { useState, useEffect } from "react";

export const useFetch = (url) => {
    const [state, setState] = useState(initialState);
    const [state2, setState2] = useState(initialState);
    const getData = async() => {
        const response = await fetch(url);
        const data = await response.json();
        setState(modifiedState);
        setState(modifiedState2);
    };
    useEffect(() => {
        getData();
    }, [])
    return [state, state2];
}
```

Simply this hook can be import and used into your react projects just like any other react hook.

```
import React from "react";
import ReactDom from "react-dom";
import { useFetch } from "useFetch";

const App = () => {
    let url = 'https://api.github.com/users/grady2002';
    const [state, state2] = useFetch(url);
    return null;
}

ReactDom.render(
    <App />,
    document.getElementById("root");
)
```
