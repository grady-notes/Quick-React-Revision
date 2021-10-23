# Children

children is a keyword of the props which is used to read manually stored data in the component that is different from the component attribute.

```
import React from "react";
import ReactDom from "react-dom";

const Paragraph = () => {
    return (
        <React.Fragment>
            <Information>
                <p>I am children prop</p>
            </Information>
        </React.Fragment>
    );
}

const Information = (props) => {
    return(
        {props.children}
    );
}

ReactDom.render(
    <Paragraph />,
    document.getElementById("root");
)
```

Anything inside the &lt;Information&gt;...&lt;/Information&gt; will be rendered as the data because of the {props.children} keyword.
