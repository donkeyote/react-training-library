---
id: anatomy-of-a-react-application
title: Anatomy of a React Application
---

Now we can start to have a wander around the folders of our react app and see what it's made up of and where our code will live.

## public

The ```public``` folder houses the entry point into our application, ```index.html```. For now we can ignore the rest of the files. Open the ```index.html``` file and update the content of the meta description tag and the title to personalise your app.

We should also pay attention to a little div with an id of _root_ that can be found on the page:

```html
<div id="root"></div>
```

It's in this div that we will now place our react app!

## src

The ```src``` folder will store all our source code and is the only location our build and start scripts will look in. This folder must also always contain an ```index.tsx``` file which will be our TypeScript entry point.

Lets create that ```index.tsx``` file and add a hello world message:

```tsx
import React from 'react';
import ReactDOM from 'react-dom';

ReactDOM.render(<div>Hello World</div>, document.getElementById('root'));

```

Our new entry point for the app just needs to make a call to ```ReactDOM.render``` which will add a React element into the DOM. The first argument is the element we wish to add while the second argument is the parent element that will contain the element. So for our code above we are adding a message of Hello World into the div with an id of root that we just found in the ```index.html``` file. The React DOM package will rarely be needed outside our entry point until we look at some more advanced concepts.

Now you can go ahead and run ```npm run start``` or ```yarn start```. This will open your new app in your default browser and just display Hello World. Note that the title of the browser tab will reflect the value you set in ```<title />``` tag earlier

## build

The last folder to be aware of is the ```build``` folder. This will only appear when you run ```npm run build``` or ```yarn build```. If you explore that folder you will find all the assets you need to deploy your site, including the public files and the JavaScript files which have been transpiled from TypeScript and minified.
