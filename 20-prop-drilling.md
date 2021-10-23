# Prop Drilling

Prop Drilling is the process of passing function or props all the way down to another functions for them to be used. This can be well managed in lesser components, but it can also be a lot more chatoic in multiple components or complete applications.

```
import React, { useState } from "react";
import ReactDom from "react-dom";

const PropDrilling = () => {
    const [people, setPeople] = useState(somedata);
    const removePerson = (id) => {
        setPeople((people) => {
            return people.filter((person) => {
                id !== id
            });
        })
    }
    return(
        <React.Fragment>
            <List people = {people} removePerson = {remove} />
        </React.Fragment>
    );
}

const List = ({people, removePerson}) => {
    return (
        <React.Fragment>
            {people.map((person) => {
                return(
                    <SinglePerson
                        key={id}
                        {...person}
                        removePerson = {remove}
                    />
                );
            })}
        </React.Fragment>
    );
}

const SinglePerson ({id, name, removePerson}) => {
    return (
        <div>
            <h4>{name}</h4>
            <button onClick={() => removePerson(id)}>
                Remove Person
            </button>
        </div>
    );
}

ReactDom.render(
    <PropDrilling />,
    document.getElementById("root");
);
```

In this snippet, the removePerson function had to be passed all the way down as a prop which created a mess. We can avoid this unwanted prop drilling with the help of the useContext hook.
