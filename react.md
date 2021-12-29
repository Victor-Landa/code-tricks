Create react app with TypeScript
```bash
npx create-react-app . --template typescript
```

Redirect with history hook.
```javascript
import { useHistory } from 'react-router-dom';

const history = useHistory();

const redirectTo = () => {
  history.push('http://localhost:4000/products');
}
```

useReducer
1. Create a component
2. Create the initial state
3. Create the reducer

Folder structure
- reducer
  - actions
    - actions.ts
  - interfaces
    - interfaces.ts
  - state
    -state.ts
  Reducer.tsx