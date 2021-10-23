# React Router - Basic Routing

```
import React from "react";
import ReactDom from "react-dom";
import {
    BrowserRouter as
    Router, Route
} from "react-router-dom";

const BasicRouting = () => {
    return (
        <Router>
            <Route exact path="/">
                <h1>Home</h1>
            </Route>
            <Route path="/about">
                <h1>About</h1>
            </Route>
        </Router>
    );
}

ReactDom.render(
    <BasicRouting />,
    document.getElementById('root');
);
```
