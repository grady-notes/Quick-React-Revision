# React Router - Error Page & Switch

Switch comes into place when a user goes searching for a place that doesnt exist and instead of that, an error page has to be displayed over there. This error page behaves like a 404 page. The path of this error page is denoted by an asterix (\*)

```
import React from "react";
import ReactDom from "react-dom";
import {
    BrowserRouter as
    Router, Route, Switch
} from "react-router-dom";

const SwitchExample = () => {
    return (
        <Router>
            <Switch>
                <Route exact path='/'>
                    <h1>Home</h1>
                </Route>
                <Route path='/about'>
                    <h1>About</h1>
                </Route>
                <Route path='*'>
                    <h1>Error</h1>
                </Route>
            </Switch>
        </Router>
    );
}

ReactDom.render(
    <SwitchExample>,
    document.getElementById("root");
);
```
