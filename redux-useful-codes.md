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
_Important: We can't use useEffect when we have a return on our component._

Access to state from components.
```javascript
import { useSelector } from 'react-redux';

const itemsOnState = useSelector(state => state.items);
```
