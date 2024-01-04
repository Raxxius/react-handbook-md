# Baw Medical React Handbook - Patterns and Design Style

### 1. Technology Stack:

Utilize Vite as the project setup tool, JavaScript as the primary language, Babel for transpilation, ESLint for code linting, Prettier for code formatting, and Jest for testing within React projects.


### 2. Folder Structure and Micro Frontend Design Pattern:

Adopt a recommended folder structure, following the Micro Frontend design pattern for better organization and scalability.


### 3. React Component Structure:

Structure React components using SOLID programming principles, emphasizing Single Responsibility, Open-Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion.

### 4. Compartmentalization and Micro Frontend Design:

Embrace the concept of compartmentalization in line with Micro Frontend design. Break down large components into smaller, more manageable subcomponents, enhancing modularity and reusability.


### 5. Separation of Concerns:

Implement separation of concerns via well-defined component layers. Logic layer handles state and business logic, Display layer manages UI rendering, Component layer orchestrates the overall structure, and Subcomponents handle specific UI elements or functionalities.


### 6. Functional Components and ES6 Syntax:

Prefer using functional components over class components. Leverage ES6 syntax for concise and expressive code.


### 7. Props and State:

Prioritize the use of variables passed via props over maintaining state within subcomponents. Reserve state for the necessary layers such as the global, page, or parent component. State should be stored at the appropiate layer to ensure readability of code. 


### 8. Basic File Structure:

Establish a clear file structure that follows the progression of component layers - Logic layer (handles state and logic), Display layer (manages UI rendering), Component layer (orchestrates structure), and SubComponent layer(s) (handles specific UI elements).


## Summary

By adhering to these guidelines, Baw Medical can create React components and projects that are not only well-structured and maintainable but also align with modern best practices and industry standards.