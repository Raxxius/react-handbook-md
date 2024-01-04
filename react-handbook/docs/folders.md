# Folder Structure

When organising a new React Project, please adhere to the following folder structure

```
  ├── node_modules
  ├── public
  └── src
    ├── _api
    ├── _tests
    ├── _docs
    ├── assets
    ├── components
    | └── subcomponents
    ├── pages
    └── hooks

```

## Folder composition

Please use the folders in the following order

## _api

the API folder contains all logic

prefer use of async await Fetch requests to call API data

example

    async function exampleFetchApi() {
    const response = await fetch("url to be fetched");

    const data = await response.json();
    return data;
    }

## _test

Store all unit tests in the _test folder

## _docs

docs are to be stored in markDown as .md files.

critical docs that are needed 

1. dependencies.md - All dependencies that are installed need to be noted in this file in the following format

```    
[ExampleDependency](url of example dependency)
used in exampleFunction.js ExampleComponent
*purpose of dependency*
```

## assets

store all assets e.g. images/logos in the assets folder

## components

Component folder should contain all components for the project, this includes anything that's not a custom hook or an API. 

React components should be written in CapitalCase.jsx files.
non-react components should be in camelCase.js files.

For complex components requring numerous unique subcomponents a subcomponent folder of the name of the primary component should be created.

In the case of a large number of generic sub components (e.g. a styled button), a subcomponent folder can be created.


## pages

When mangaging the display of multiple components a display layer is prefered to using the App.jsx file

Page files should be written in .jsx and named in CaptialCase.jsx


## hooks

Any custom hooks can be stored in this folder.


## Other folders

If other folders are required for any reason make a note in the docs folder. 
