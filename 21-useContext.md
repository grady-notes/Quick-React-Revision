# useContext

With the help of this hook, we can avoid prop drilling by simply creating a contex provider and assigning it the value for which the prop drilling was used earlier.

```
import React, { useState, useContext } from "react";
import ReactDom from "react-dom";

const PersonContext = createContext();

const ContextAPI = () => {
    const [people, setPeople] = useState(somedata);
    const removePerson = (id) => {
        setPeople((person) => {
            return people.filter((person) => {
                person.id !== id;
            });
        });
    }
    return(
        <PersonContext.Provider value={removePerson, people}>
            <h3>Context API</h3>
            <List />
        </PersonContext.Provider>
    );
}

const List = () => {
    const mainData = useContext(PersonContext);
    return(
        <React.Fragment>
            {mainData.people.map((person) => {
                return(
                    <SinglePerson
                        key={person.id}
                        {...person}
                    />
                );
            })}
        </React.Fragment>
    );
}

const SinglePerson = ({id, name}) => {
    const {removePerson} = useContext(removePerson);
    return (
        <React.Fragment>
            <div>
                <h4>{name}</h4>
                <button onClick{() => removePerson(id)}>
                    Remove person
                </button>
            </div>
        </React.Fragment>
    );
}

ReactDom.render(
    <ContextAPI />,
    document.getElementById("root");
);
```

In this snippet, instead of passing the removePerson function all the way down, we created a context which refers to the removePerson function globally.
