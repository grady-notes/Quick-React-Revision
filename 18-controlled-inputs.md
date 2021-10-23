# Controlled Inputs

```
import React, { useState } from "react";
import ReactDom from "react-dom";

const ControlledInputs = () => {
    const [firstName, setFirstName] = useState('');
    const [email, setEmail] = useState('');
    const [people, setPeople] = useState('');
    const handleSubmit = (e) => {
        e.preventDefault();
        if (firstName && email) {
            const person = {firstName, email};
            setPeople((people) => {
                return [...people, person];
            });
            setFirstName("");
            setEmail("");
        } else {
            {alert('Empty Values')};
        }
    };
    return(
        <React.Fragment>
            <form onSubmit={handleSubmit}>
                <input placeholder="name" />
                <input placeholder="email" />
                <button>Add Person</button>
            </form>
            {people.map((person) => {
                const {id, firstName, email} = people;
                return (
                    <h4>{firstName}</h4>
                );
            })}
        </React.Fragment>
    );
}

ReactDom.render(
    <ControlledInputs />,
    document.getElementById("root");
);
```
