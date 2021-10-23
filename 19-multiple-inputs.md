# Multiple Inputs

```
import React, { useState } from "react";
import ReactDom from "react-dom";

const MultipleInputs = () => {
    const [person, setPerson] = useState({
        firstName: "",
        email: "",
        age: ""
    });
    const [people, setPeople] = useState([]);
    const handleChange = (e) => {
        const name = e.target.name;
        const value = e.target.value;
        setPerson({
            ...person,
            [name]: value
        })
    }
    const handleSubmit = (e) => {
        e.preventDefault();
        const newPerson = {
            ...person,
            id: new Date().getTime().toString()
        };
        setPeople([...people, newPerson]);
        setPerson({
            firstName: '',
            email: '',
            age: ''
        });
    }
    return (
        <React.Fragment>
            <form>
                <input
                    type="text"
                    name="firstName"
                    value={person.firstName}
                    onChange = {handleChange}
                />
                <input
                    type="text"
                    name="email"
                    value={person.email}
                    onChange = {handleChange}
                />
                <input
                    type="text"
                    name="age"
                    value={person.age}
                    onChange = {handleChange}
                />
                <button type="submit" onClick={handlesubmit}>
                    Add Person
                </button>
            </form>
            <div>
                {people.map((person) => {
                    const {
                        id,
                        firstName,
                        email,
                        age
                    } = person;
                    return (
                        <div key={id}>
                            <h4>{firstName}</h4>
                            <p>{email}</p>
                            <p>{age}</p>
                        </div>
                    );
                })}
            </div>
        </React.Fragment>
    );
}

ReactDom.render(
    <MultipleInputs />,
    document.getElementById("root");
);
```
