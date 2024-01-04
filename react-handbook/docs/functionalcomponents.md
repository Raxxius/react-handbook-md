# React Components Overview

1. React components should be written as functional components
2. Large components should be broken into subcomponents
3. Subcomponents should be stateless
4. Stateless components should be written as arrow functions for concise code.

## Functional Components

React components are best written as functional components. The preferred syntax is to use arrow functions, especially for stateless components where implicit returns contribute to more concise code.

### Destructuring props

Always destructure props rather than use props.var, this makes it easier to read what is being passed to the component. Either destructure the props in the function()(prefered) or as a first variable. e.g.

preferred:

        const Component1 = ({time, date}) => (
            <div>{time} {date}</div>
        )

alternative:

        const Component1 = (props) => {
            const {time, date} = props
            return (
                <div>{time} {date}</div>
            )
        }

The preferred approach, directly destructuring within the function parameters, is generally recommended for its brevity and clarity and in the case of SubComponents allows for direct returns. However, the alternative approach, destructuring as the first step inside the function body, is also acceptable and might be preferred in certain scenarios.

This practice ensures a standardized and easily understandable way of handling props, contributing to a more consistent and readable codebase.

## Subcomponents

React subcomponents should be composed via Arrow functions, with props passed from a the parent. 

React states should not be set in subcomponent layers. 

example stateless component:

        const Component1 = ({ count, updateCount }) => (
            <div className="count-controller-box">
                <p className="count-text">count is {count}</p>
                <button onClick={() => updateCount(count + 1)}>+1</button>
                <button onClick={() => updateCount(count - 1)}>-1</button>
            </div>
        );

In this component the props count (a number) and updateCount (a function that uses parent state). The use of an Arrow function allows for an [implicit return](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#function_body).
