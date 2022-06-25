# Creat React App
---
## App.js
``` javascript
import './App.css';

function App() {

  let name = "김용진";

  return (
    <div className="App">
      <header className="App-header">
        <h2> 안녕 리액트 {name}</h2>
      </header>
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
