## SOLID Principles and React

SOLID principles as implimented in a React project can be summarised as follows.


### Single Responsibility Principle

*Highly important*

All components should strictly adhere to Single Responsibility Principle.

Specific to React this means:

1. All components should perform a single feature
2. Complex components with multiple features should be broken up into a organisation layer and sub components for each feature
3. Basic program layer structure is as follows:

    a. Data management layer
    b. User interface layer
    c. React Component layer


### Open Closed Principle 

*Important*

In most cases components and subcomponents should be open to extension but closed to modification.

Specific to React this means:

1. Extension is provided by the use of props over use of state


### Liskov Substitution Principle 

*Relatively important*

While functional components don't have class based inheritence like classical OOP languages, passing of props from parent to child props can still allow React components to obey the Liskov Subsitution principle.

Specific to React this means:

1. When extending a component, props are passed through the parent to child, utilising composition over inheratance.

        const Button = (name, function) {
            <div 
                className="button" 
                onClick={function}
            >
            {name}
            </div>
        }

    to 

        const NeonButton = (name, function, colour) {
            <div className={colour}>
                <Button name={name}
                    function={function} 
                />
            </div>
        }

    The NeonButton extends the button Component by wrapping it in a div with an extra feature, the buttons props are passed down from the parent NeonButton to the Button, should the Button component be changed, the NeonButton will only need to be changed if Button requires additional props, and then only by passing props.

    The Liskov Subsititution Principle is a key design pattern for React.


### Interface segregation principle

*Important*

Generally try to keep interface components simple, this concept works in tandem with the Single Responsibility Principle.

Specific to React this means:

1. Only ever pass relevant props to child components. Destucturing props at component layers helps with this.

