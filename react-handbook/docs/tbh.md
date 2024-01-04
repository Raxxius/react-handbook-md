# State variables and logic

## useState

use the The [general rules of useState](https://react.dev/reference/react/useState) when declaring variables.

As a design pattern state should be used in one of three layers:

1. Global variables (such as login details, API calls that are used in multiple pages etc) should be located in the App.jsx 
2. Page specific varaibles should be present in the appropiate Page.jsx
3. Components that require their own state should have that stored in the appropite Component.jsx 
4. Subcomponents should not have their own state

By having 3 distinct layers where state can be found, it should be realtively simplistic to determine where the state logic being passed to components dervives from

In the interest of maintaining modularity, store state at the lowest level possible, excluding the subcomponent level. This approach ensures that state logic is localized to the most relevant component or layer, facilitating a clearer understanding of where the state is derived.


## Conditional logic styling

When implementing conditional logic in JavaScript, it is recommended to favor the [ternary operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_operator) or [switch statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch) over traditional [if/else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else) statements. The choice between these constructs should be made based on the specific use case and readability.

Ternary operators provides a concise and easily readable alternative to if/else statements. It is particularly useful for simple conditional checks.

Example:

        const result = condition ? 'Value for true' : 'Value for false';


In the case of complex case logic with multiple outcomes, switch statements provide clear readability and a default case for fallback/error handling.

Example:

        switch (day) {
          case 'Monday':
            // Logic for Monday
            break;
        case 'Tuesday':
            // Logic for Tuesday
            break;
        // Additional cases
        default:
            // Default case
        }


Generally avoid if/else statements, as readability can be an issue.

