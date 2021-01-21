###### *This article is sponsored by [Flutterwave](https://dashboard.flutterwave.com/signup?referrals=RV686851) - Flutterwave is the easiest way to make and accept payments both online and offline from customers anywhere in the world. It is absolutely free!*

---
React has a couple of folders set up configured already after the installation of the starter React app.

> Files, folders, and dependencies are installed by the **create-react-app** tool.

---
### Folder Structure
#### package.json file
The file contains 3 major modules **react**, **react-dom**, and **react-script**. For example, `react-script` is responsible for the app build. The `react-script` can be used to start the app server, build, store or deploy an app, test an app, eject all current and future installed dependencies in the file, *package.json*.

> You can not undo the ejection operation. So avoid the command `npm eject` for now! The command `npm start` will be used more often to run the server.

**package.json**
```json
{
  "name": "my-app",
  "version": "0.1.0",
  "private": true,
  "dependencies": {
    "@testing-library/jest-dom": "^5.11.6",
    "@testing-library/react": "^11.2.2",
    "@testing-library/user-event": "^12.6.0",
    "react": "^17.0.1",
    "react-dom": "^17.0.1",
    "react-scripts": "4.0.1",
    "web-vitals": "^0.2.4"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  },
                          ...    ...    ...
                          ...    ...    ...
                          ...    ...    ...
}
```

> Anytime you install any dependencies, the *package.json* adds them to the **JSON** (**JavaScript Object Notation**) object automatically

The `react-dom` module gives access to all `ReactDOM` APIs, `import ReactDOM from 'react-dom'` like rendering components to the **DOM** (**Document Object Model**). The `react` module must be installed before you get access to the `react-dom` module. 

#### eslintConfig
The *eslintConfig* is a package used with both the **eslint-plugin-react** and **Jest rules** to support React syntax. It allows the linting to warn in case of errors.

```json
},
"eslintConfig": {
  "extends": [
    "react-app",
    "react-app/jest"
  ]
},
                          ...    ...    ...
                          ...    ...    ...
                          ...    ...    ...
}
```

#### node_module
The folder holds dependencies and sub-dependencies of the modules `react`, `react-dom` and `react-script` in the *package.json* file.
Avoid editing files and folders! The entire app relies on the folder.

#### public folder
The root folder contains few files such as *index.html*, *favicon.ico*, *manifest.json*, and images for the app icon for different browsers and OS.

The *index.html* contains the root element `<div id="root"></div>`. This is where components from the *index.js* file are mounted before rendered to the screen.

Since the tool, **Create React App** gives a progressive app out of the box, the *manifest.json* file allows us to define some metadata about our app. 

More metadata can be added to the head element. Notice there is no script element in the *index.html*. This is because **NPM** installed the `create-react-app` package that contains the script metadata in form of dependencies. This means you can [integrate React with any library](https://techstack.hashnode.dev/react-bootstrap-integration), be it **CSS** (**Cascading Style Sheet**) library like Bootstrap, JavaScript library like **jQuery** (not recommended), etc via `npm` instead of manually adding them in the metadata. For example, the command `npm install bootstrap`.

**public/index.html**
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <meta
      name="description"
      content="Web site created using create-react-app"
    />
    <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />
    <!--
      manifest.json provides metadata used when your web app is installed on a user's mobile device or desktop. See https://developers.google.com/web/fundamentals/web-app-manifest/
    -->
    <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
    <!--
      Notice the use of %PUBLIC_URL% in the tags above.
      It will be replaced with the URL of the `public` folder during the build. 
      Only files inside the `public` folder can be referenced from the HTML.
Unlike "/favicon.ico" or "favicon.ico", "%PUBLIC_URL%/favicon.ico" will
      work correctly both with client-side routing and a non-root public URL.
      Learn how to configure a non-root public URL by running `npm run build`.
    -->
    <title>React App</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
    <!--
      This HTML file is a template.
      If you open it directly in the browser, you will see an empty page.
You can add webfonts, meta tags, or analytics to this file.
      The build step will place the bundled scripts into the <body> tag.
To begin the development, run `npm start` or `yarn start`.
      To create a production bundle, use `npm run build` or `yarn build`.
    -->
  </body>
</html>
```
> Try to inspect the root element in future articles to notice nested elements injected into it when creating an app in React.

#### src folder
The *src* folder contains files to edit.

**App.js**

```jsx
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;
```

Edit the *App.js*.

**App.js**
```jsx
import React from "react";
import "./App.css";

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <h3>Hello World</h3>
        <p>
          You are now editing the <code>App.js</code> file
        </p>
      </header>
    </div>
  );
}

export default App;
```
> Exit the server with `ctrl` + `c`.
**Happy Coding!!!**

---
[![Buy me a Coffee](https://res.cloudinary.com/bizstak/image/upload/v1610317510/ko-fi-trans_fr3su4.png)](https://www.buymeacoffee.com/bellotech) 

---
#### Techstack | Flutterwave 
Techstack article, sponsored by Flutterwave. Flutterwave is the easiest way to make and accept payments both online and offline from customers anywhere in the world. It is absolutely free!  Also, you get a Flutterwave dollar barter card when you [signup](https://dashboard.flutterwave.com/signup?referrals=RV686851). Open an online store and take your business anywhere in the world.

[Check out the demo](https://youtu.be/ClXVUM3Rf7A)

[Sign up today to get started](https://dashboard.flutterwave.com/signup?referrals=RV686851)

[Support](https://dashboard.flutterwave.com/donate/3lo9klliqwbu) what I do and push me to keep making free content.
