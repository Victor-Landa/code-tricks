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
