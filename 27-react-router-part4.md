# React Router - Link Component

Instead of traditional anchor tag from the HTML we can use the Link component from the react router to make the navigation a whole lot easier and much faster.

```
import React from "react";
import ReactDom from "react-dom";
import { Link } from "react-router-dom";

const LinkBasics = () => {
    return (
        <Link to="/about">
            Visit About Section
        <Link>
    );
}

ReactDom.render(
    <LinkBasics />,
    document.getElementById("root");
);
```
