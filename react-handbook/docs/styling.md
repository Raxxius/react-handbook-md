# CSS and styling


## CSS location

CSS is to be held in seperate files and not inline.

CSS is to be held at three levels:

1. Global scoped CSS is to be stored in the App.css file, this includes the sites fonts and basic styling, such as themes. From a default Vite build, merge the index.css file into the App.css.
2. Page specific CSS is to be stored in the appropriate Page.css file,
3. Component specific CSS is to be stored at the Component level and it to be regulated by CSS modules to avoid potentially unwanted side effects.
4. Reactive CSS are generaly to be engaged by Javascript changes to components class. 

## CSS conventions

### Global Scope

Global scope CSS include theme colours, colour scheme, fonts, basic html element styling etc.

### Page Scope

Page scoped CSS is generally concerned only with the display of components on the page.

### Component Scope

In accordance with microfrontends design patterns, Component.jsx are to have a component.css file associated with them. 

Vite by default supports CSS modules via Lightning CSS

## Media Queries

For responsive web design, utilise the design pattern of starting with css for phones, then moving onto pads, laptops and large screen media.

Use the following breakpoints:

    @media (min-width: 768px)
    @media (min-width: 1024px)
    @media (min-width: 1280px)

this will accomodate phones, pads, laptops and large screen monitors.
