Redirect with history hook.
```javascript
import { useHistory } from 'react-router-dom';

const history = useHistory();

const redirectTo = () => {
  history.push('http://localhost:4000/products');
}
```
