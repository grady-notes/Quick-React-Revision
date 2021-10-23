# Rendering objects and components using map()

Each and every item in the return of the map() should have the key? attribute to differentiate it from the other items.

```
import React from "react";
import ReactDom from "react-dom";

const books = [
    {
        title: "Harry Potter",
        author: "JK Rowling",
    },
    {
        title: "Time Machine",
        author: "HG Wells",
    },
];

const Book = (props) => {
    const {title, author} = props.book;
    return (
        <React.Fragment>
            <h1>{title}</h1>
            <h3>{author}</h3>
        </React.Fragment>
    );
}

const BookList = () => {
    return (
        <React.Fragment>
            <section>
                {books.map((book) => {
                    const {title, author} = book;
                    return (
                        <Book
                            book={book}
                            key={
                                new Date().getTime().toString()
                            }
                        />
                    );
                })};
            </section>
        </React.Fragment>
    );
}

ReactDom.render(
    <BookList />,
    document.getElementById("root");
);
```

This snippet will render each and every item in the books array as a seperate book component with the help of the map function without us having to repeat the entire procedure again and again. If you want to add any other book, you can simply add the book details in the array in the Object format.
