# Props
---

## Counter.js
``` javascript
import React, { useState } from "react";
import OddEvenResult from "./OddEvenResult";

const Counter = ({initialValue}) => {

    const [count, setCount] = useState(initialValue);

    const onIncrease = () =>{
        setCount(count + 1);
    };

    const onDecrease = () =>{
        setCount(count - 1);
    };

    return (
        <div>
            <h2>{count}</h2>
            <button onClick={onIncrease}>+</button>
            <button onClick={onDecrease}>-</button>
            <OddEvenResult count = {count} />
        </div>
    );
};

Counter.defaultProps={
    initialValue:0
}

export default Counter;
```

## OddEvenResult.js
``` javascript
const OddEvenResult = ({count}) => {
    console.log(count);
    return <>{count % 2 === 0 ? "짝수" : "홀수"}</>
}

export default OddEvenResult;
```

## Container.js
``` javascript
const Container = ({children}) => {
    console.log(children);
    return (
    <div style={{margin:20, padding:20, border:"1px solid gray"}}>
        {children}
    </div>
    );
};

export default Container;
```

## App.js
``` javascript
import React from 'react';
// import './App.css';
import MyHeader from './MyHeader';
import MyFooter from './MyFooter';
import Counter from './Counter';
import Container from './Container';

function App() {
  const number = 5;

  const counterProps = {
    a:1,
    b:2,
    c:3,
    d:4,
    e:5,
  }

  return (
    <Container>

      <div>
        <MyHeader />
        <MyFooter />
        <Counter {...counterProps} />
      </div>
    </Container>
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
