# useState array

```
import React, { useState } from "react";
import ReactDom from "react-dom";

const data = [
    {id: 1, name: "Aatif"},
    {id: 2, name: "Grady"},
    {id: 3, name: "Raymond"}
];

const UseStateArray = () => {
    const [people, setPeople] = useState(data);
    const removeItem = (id) => {
        let newPeople = people.filter((person) => {
            person.id !== id
        });
        setPeople(newpeople);
    };
    return (
        <React.Fragment>
            {
                people.map((person) => {
                    const [id, name] = person;
                    return (
                        <div key={id}>
                            <h4>{name}</h4>
                            <button onClick={() => {removeItem(id)}}>
                                Remove
                            </button>
                        </div>
                    );
                })
            }
            <button onClick = {() => {
                setPeople([]);
            }}>Clear</button>
        </React.Fragment>
    );
}

ReactDom.render(
    <UseStateArray />,
    document.getElementById("root");
);
```

The above snippet will render the data array and display a button to remove the individual items along with each of the displayed items. This button will remove the current item from the array and a new array will be displayed without the recently removed item. Also there is a sperate individual button to clear out everything from the array and display an empty set.
