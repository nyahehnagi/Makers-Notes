# Javascript Cheat Sheet

## Node/Jest Set Up

- `npm init` initialises `package.json` in project directory
- `npm install` to install libraries from package.json 
- `npm install --save jest` to install jest
- `npm install -g esbuild` install esbuild globally
- `npm run build` to create `bundle.js`

need the below in package.json to run a build
~~~~
"scripts": {
  // ...
  "build": "esbuild index.js --bundle  --outfile=bundle.js --watch"
},
~~~~

## Simple Server
- `npm install express` install express 

## Index.html
-  `<script type="text/javascript" src="bundle.js"></script>` Need this to get the javascript into the page
## Views
- Pass model and api into the constructor of a view
- `this.mainContainerEl = document.querySelector('#main-container');` to set the main container element - useful for everything else.
- Add event listeners to buttons etc
~~~~
- `this.element.addEventListener('click', () => {
      // do something
    });
~~~~
- `const noteEl = document.createElement('div')` creates an element of type div
- `document.querySelector('#add-note')` to find an element with id
- `document.querySelector('.add-note')` to find an element by class name

### Testing Views
- `const fs = require('fs');` needed to read the index.html
- `document.body.innerHTML = fs.readFileSync('./index.html');` loads index.html so the document can be used in tests



