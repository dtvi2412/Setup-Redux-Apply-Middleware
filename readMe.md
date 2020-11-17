# Setup Redux


## Install Redux React-Redux

```bash
npm install redux react-redux
```

## Import file
```bash
import { createStore, applyMiddleware, compose } from "redux";
import { Provider } from "react-redux";
import RootReducer from "./Redux/Reducers/root";
import thunk from "redux-thunk";

```

## Defind Varible 

```bash
const composeEnhancers = window.__REDUX_DEVTOOLS_EXTENSION_COMPOSE__ || compose;
const store = createStore(
  RootReducer,
  // window.__REDUX_DEVTOOLS_EXTENSION__ && window.__REDUX_DEVTOOLS_EXTENSION__()
  // applyMiddleware(thunk)
  //Su dung redux thunk middleware voi devtool
  composeEnhancers(applyMiddleware(thunk))
);
```

##  Apply Provider 

```bash
<Provider store={store}>
{" "}
<App />
</Provider>,
```
<div style="page-break-after: always;"></div>

## Image Redux


![image info](https://miro.medium.com/max/2880/1*T0kjwacFHNZ_p8AC2lv-iA.jpeg)