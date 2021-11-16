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

Countdown
```javascript
// Set the countdown limit
const countDownLimit = new Date().setHours('22', '30', '00');

// Update the count down every 1 second
const countDownInterval = setInterval(function() {
  // Get today's date and time
  const now = new Date().getTime();

  // Find the distance between now and the count down date
  const distance = countDownLimit - now;

  // Time calculations for days, hours, minutes and seconds
  const days = Math.floor(distance / (1000 * 60 * 60 * 24));
  const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  const seconds = Math.floor((distance % (1000 * 60)) / 1000);

  // Output the result
  console.log(`${days}d ${hours}h ${minutes}m ${seconds}s`);

  // If the count down is over
  if(distance < 0) {
    clearInterval(countDownInterval);
    console.log('Expired');
  }
}, 1000);
```