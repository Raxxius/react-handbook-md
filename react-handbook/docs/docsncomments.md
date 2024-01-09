# Documentation and Comments

Accurate documentation is critical for

Well-paced comments in code are crucial for maintaining a clear and structured codebase.


## Essential Documents

It is essential to have a document with all used depencencies and working version, while this information can be gleened from the package-lock.js this file can become quite verbose as it includes all react depencies such as babel.


## Comments in code

The preference is to comment code with short concise statements that improve clarity and allow for new contributors to quickly establish the 

Comments are also used to organise React.jsx files. 


### Comments at start of function.jsx files

A brief paragaph at comment at the start of function.js files should provide an overview of the file's purpose, inputs, functionality and other relevant details.

Also do this for subcomponents.

Example:

        checkLogin.js
        /**
        * Manages login functionality through API integration.
        * 
        * Function:
        * - `handleLogin`: Processes login request, integrating with an API.
        * 
        * Input Variables:
        * - `username`: Login username.
        * - `password`: Login password.
        * 
        * Output:
        * - Returns `true` on successful login, `false` otherwise.
        */

        import React from 'react';
        import API from './api.js';

        const checkLogin = ({ username, password }) => {
        // Rest of the code
        };

### Comments in jsx files

Use of comments to organise code sections of React components.

Example:

        const ExampleApp = () => {
        /** Props Destructring */
        // if props are passed down as 'props', destructure them first

        /** State */
        // UseState should be defined here

        /** Custom State Functions (generally use imports)*/
        // state functions

        /** useEffect hooks */
        // useEffects here to setup state

        /** core return */
        return (
            //return code.
        )
        }