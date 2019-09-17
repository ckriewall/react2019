# react2019

A project for testing best practices in React. You can clone the repo for a working project, or perform the manual installation to practice scaffolding a modern app.

## Getting Started

### Clone the Repo

Clone this repo for a React app with support for:

- [Font Awesome](https://fontawesome.com) - Easy icons
- [React Bootstrap](https://react-bootstrap.github.io/) - Styling
- [React Router](https://reacttraining.com/react-router/) - SPA routing

### Manual Installation

If you'd rather build this app from scratch, perform the steps below.

#### Run create-react-app

```bash
npx create-react-app myproject
```

##### Clean up Junk

```bash
rm -i src/App.css src/App.test.js src/index.css src/logo.svg src/serviceworker.js
```

In `src\App.js` delete...

```javascript
import logo from './logo.svg';
import './App.css';
```

In `src\index.js` delete...

```javascript
import './index.css';
```

and

```javascript
import * as serviceWorker from './serviceWorker';
```

and

```javascript
// If you want your app to work offline and load faster, you can change
// unregister() to register() below. Note this comes with some pitfalls.
// Learn more about service workers: https://bit.ly/CRA-PWA
serviceWorker.unregister();
```

#### Install Font Awesome

- Create a [Font Awesome Kit](https://fontawesome.com/start)
- Copy the kit code, e.g:

  `<script src="https://kit.fontawesome.com/<my_kit_id>.js"></script>`

- Paste the kit code into `public\index.html`

```html
<link rel="apple-touch-icon" href="logo192.png" />
<link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
<script src="https://kit.fontawesome.com/<my_kit_id>.js"></script>
<title>React App</title>
```

#### Install Bootstrap and React-Bootstrap

```bash
yarn add react-bootstrap bootstrap
```

#### Install React Router

```bash
yarn add react-router-dom
```

#### Update dependencies

```bash
yarn install
```

#### Define React Functional Components with arrow functions

- Define [`src\nav\HeaderNav.js`](https://github.com/ckriewall/react2019/blob/master/src/nav/HeaderNav.js) - with Bootstrap navigation
- Define [`src\Home.js`](https://github.com/ckriewall/react2019/blob/master/src/Home.js)
- Define [`src\About.js`](https://github.com/ckriewall/react2019/blob/master/src/About.js)
- Define [`src\data\DataList.js`](https://github.com/ckriewall/react2019/blob/master/src/data/DataList.js) - with an `axios` API call
- Define [`src\data\DataItem.js`](https://github.com/ckriewall/react2019/blob/master/src/data/DataItem.js)

#### Configure Routes in `src\App.js`

```jsx
import React, { Fragment } from 'react';
import { BrowserRouter, Route } from 'react-router-dom';
import Navbar from './nav/HeaderNav';
import About from './About';
import Home from './Home';
import DataList from './data/DataList';
import Container from 'react-bootstrap/Container';

function App() {
  return (
    <BrowserRouter>
      <Fragment>
        <Navbar />
      </Fragment>

      <Container>
        <Route exact path='/' component={Home} />
        <Route path='/about' component={About} />
        <Route path='/data' component={DataList} />
      </Container>
    </BrowserRouter>
  );
}

export default App;
```

#### Run the application

```bash
yarn start
```

## Deployment

Add additional notes about how to deploy this on a live system

## Versioning

We use [SemVer](http://semver.org/) for versioning.

## Authors

- _Initial work_ - [C Kriewall](https://github.com/ckriewall)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

- [React Front to Back](https://www.udemy.com/modern-react-front-to-back/) by [Traversy Media](https://www.traversymedia.com/)
