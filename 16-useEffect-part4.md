# useEffect - Fetching Data

```
import React, { useState, useEffect } from "react";
import ReactDom from "react-dom";

let url = 'https://api.github.com/users/grady2002';

const UseEffectFetch = () => {
    const [users, setusers] = useState([]);
    const getUsers = async() => {
        const response = await fetch(url);
        const users = await response.json();
        setUsers(users);
    };
    useEffect(() => {
        getUsers();
    }, []);
    return(
        <React.Fragment>
            <h3>Github Users</h3>
            <ul>
                {users.map((user) => {
                    const {id, login, urlA} = user;
                    return(
                        <li key={id}>
                            <img src={urlA}>
                            <h4>{login}</h4>
                        </li>
                    );
                })}
            </ul>
        </React.Fragment>
    );
}
```

This snippet will fetch the data from the API as soon as the page loads, this has similar behaviour to the window.addEventListene('load', () => {}) in Javascript and $(document).load(() => {}) in jQuery
