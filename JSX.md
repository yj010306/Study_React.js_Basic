# JSX
---
## MyHeader.js
``` javascript
const MyHeader = () => {
    return <header>헤더</header>
};

export default MyHeader;
```

## MyFooter.js
``` javascript
const MyFooter = () => {
    return <footer>myfooter</footer>
}

export default MyFooter;
```

## App.css
``` css
.App {
  background-color: black;
}

h2{
  color: red;
}

#bold_text {
  color: green;
}
```

## App.js
``` javascript
// import './App.css';
import MyHeader from './MyHeader';
import MyFooter from './MyFooter';

function App() {

  let name = "김용진";

  const style = {
    App : {
      backgroundColor:'black',
    },
    h2 : {
      color:'red',
    },
    bold_text : {
      color:'green',
    },
  };

const number = 5;


  return (
    <div style={style.App}>
      <MyHeader />
      <MyFooter />
        <h2 style={style.h2}> 안녕 리액트 {name}</h2>
        <b style={style.bold_text} id="bold_text">
          {number}는 : {number % 2 === 0 ? "짝수" : "홀수"}
        </b>
    </div>
  );
}

export default App;
```

## index.js
``` javascript
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
```
