# Forms in react

In normal HTML we could submit the forms by putting an action attribute on the form which would direct the form to a separate location and reload the previous page.

But in react things are a little different when it comes to working with forms and inputs. To submit the form data, we can use either the `onClick()` function on the submit button or we can use the `onSubmit()` button on the form itself. Same as HTML, the form will reload the page once the form is submitted which will result in the loss of data. But in javscript we can prevent that by putting the `preventDefault()` method inside the function that will be handling the form data.

```
import React from "react";
import ReactDom from "react-dom";

const Form = () => {
    const handleSubmit = (e) => {
        e.preventDefault();
        console.log("Hello World");
    };
    return (
        <React.Fragment>
            <form onSubmit={handleSubmit}>
                <input type="text" placeholder="" />
            </form>
        </React.Fragment>
    );
}
```

This snippet will log "Hello World" to the console after the form is submitted without refreshing the page and preserving the form data.
