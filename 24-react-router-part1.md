# React Router - Introduction

All the previous codes and snippets were for working with single pages or in other words, they were just static pages with no interaction at all. When it comes to real life applications, we need multiple pages for an app to work properly.

In traditional HTML we would set up multiple hyperlinks that would indicate to different pages of the directory.

But in React, things get a little bit different. Since react uses virtual DOM we do not have the allowance to acces different files explicitly, all we have is a single page container. So instead of hyperlinks we would set up a router which would help us to move around the webpage freely and efficiently without having to refresh the entire webapp.

For this purpose we have the React Router. There are a lot of routing libraries available on the NPM but the React Router remains the most prominent one. We can simply use the command to install the router.

```
npm install --save react-router-dom
```

The minimum react-router-dom version must be greater than or equal to 5.2.0

To get started with the react router, we have to import the BrowserRouter from the package react-router-dom and give it an alias of Router, Switch and Route. This can simply be done with the following line.

```
import {
    BrowserRouter as
    Router, Route, Switch
} from "react-router-dom";
```
