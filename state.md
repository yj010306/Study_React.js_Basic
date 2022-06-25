# State
---

## Counter.md
``` javascript
import React, { useState } from "react";

const Counter = () => {

    // 0에서 출발
    // 1씩 증가하고
    // 1씩 감소하는
    // count 상태

    console.log("counter 호출!");

    const [count, setCount] = useState(0);

    const onIncrease = () =>{
        setCount(count + 1);
    }
    const onDecrease = () =>{
        setCount(count - 1);
    }

    const [count2, setCount2] = useState(0);

    const onIncrease2 = () =>{
        setCount2(count2 + 1);
    }
    const onDecrease2 = () =>{
        setCount2(count2 - 1);
    }

    return (
        <div>
            <h2>{count}</h2>
            <button onClick={onIncrease}>+</button>
            <button onClick={onDecrease}>-</button>

            <h2>{count2}</h2>
            <button onClick={onIncrease2}>+</button>
            <button onClick={onDecrease2}>-</button>
        </div>
    );
};

export default Counter;
```

## App.js
``` javascript
import React from 'react';
// import './App.css';
import MyHeader from './MyHeader';
import MyFooter from './MyFooter';
import Counter from './Counter';

function App() {
const number = 5;


  return (
    <div>
      <MyHeader />
      <MyFooter />
      <Counter />
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
