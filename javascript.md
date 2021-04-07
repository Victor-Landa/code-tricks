Simple array sum.
```javascript
let array = [3, 4, 5, 7];

let sum = 0;

for(let i = 0; i < array.length; i++) {
  sum += array[i];
}

return sum;
```
Validate email with regex
```javascript
!/^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$/i.test(email);
```

Conditional (Ternary) Operator (only one condition)
```javascript
error && 'There was an error'
```
String to camelCase
```javascript
function toCamelCase(str) {
  const regExp =/[-_ ]\w/ig;
  return str.replace(regExp, (match) => {
    return match[1].toUpperCase();
  });
}
```

Dispatch window resize event
```javascript
window.dispatchEvent(new Event('resize'));
```
