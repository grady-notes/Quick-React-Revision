# Your first React component.

Components in React are just made of the react import and the component function. `index.js` is the entrypoint of the react app.

```
import React from "react";
import ReactDom from "react-dom";

const Greeting = () => {
    return (
        <h1>Hello World</h1>
    );
}

ReactDom.render(
    <Greeting />,
    document.getElementByID("root");
);
```

The above snippet will render the "Hello World" text which is inside the Greeting function via the root div present in the /public/index.html file.

The HTML written in React is known as JSX, Javascript React.

# Rules to write JSX

- Returns a single element.
- Atributes in JSX must be written in camelCase.
- Close every element and use a self closing tag for the ones that do not have a distince closing tag.
