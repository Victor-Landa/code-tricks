Redux basic usage [Redux 4.1.2]
```javascript
const redux = require('redux')

const counterReducer = (state = { counter: 0 }, action) => {
  if (action.type === 'increment') {
    return {
      counter: state.counter + 1
    }
  }

  if(action.type === 'decrement') {
    return {
      counter: state.counter - 1
    }
  }

  return state
}

const store = redux.createStore(counterReducer)

const counterSubscriber = () => {
  const latestState = store.getState()
  console.log(latestState)
}

store.subscribe(counterSubscriber)

store.dispatch({ type: 'increment' }) // 1
store.dispatch({ type: 'decrement' }) // 0
```
---
Call the action from component when it loaded using useEffect.
```javascript
import React, { useEffect } from 'react';
import { useDispatch } from 'react-redux';
import { calledFunction } from './actions/allActions';

const dispatch = useDispatch();

useEffect(() => {
  const exampleFunction = dispatch( calledFunction() );
  exampleFunction();
}, []);
```
_Important: We can't use useEffect when we have a return in our component._

Access to state from components.
```javascript
import { useSelector } from 'react-redux';

const itemsOnState = useSelector(state => state.items);
```
