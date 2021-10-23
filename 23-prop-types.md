# Prop Types

Prop types allows the programmer to validate the props that are being passed onto the function or the components.

```
import React from "react";
import ReactDom from "react-dom";
import PropTypes from "prop-types";

const Product = ({image, name, price}) => {
    const url = image && image.url;
    return (
        <React.Fragment>
            <img src={url} />
            <h4>{name}</h4>
            <p>{price}</p>
        </React.Fragment>
    );
}

Product.PropTypes = {
    image: Proptype.object.isRequired,
    name: Proptype.string.isRequired,
    price: Proptype.number.isRequired,
}
Product.defaultProps = {
    name: 'Default Name',
    price: 0.00,
    image: url,
}

ReactDom.render(
    <Product image="", name="", price=0.00 />,
    document.getElementById("root");
);
```

In this snippet, we have passed three props in the Product component which are being validated by the proptypes, the image, name and price are being validated as object, string and number respoectively. Also that the default values of name, price and image are being set as 'Default Name', 0.00 and {url}.
