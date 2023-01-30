## Common JavaScript Bugs

Here are some of the most common JavaScript bugs and their causes and solutions.

### 1. Uncaught TypeError: Cannot read property 'xxx' of undefined

**Cause**: This error occurs when trying to access a property of an undefined object.

**Solution**: Check if the object is defined before accessing its properties. You can use typeof or conditional (ternary) operator to check if the object is undefined.

```js
// example
let obj;
if (typeof obj !== 'undefined') {
  console.log(obj.property);
} else {
  console.log('obj is undefined');
}

// or
console.log(typeof obj !== 'undefined' ? obj.property : 'obj is undefined');
```

### 2. Uncaught ReferenceError: xxx is not defined
**Cause**: This error occurs when trying to access a variable that hasn't been declared.

**Solution**: Declare the variable before accessing it.
```js
// example
let x;
console.log(x);
```

### 3. NaN (Not a Number)
**Cause**: This error occurs when performing mathematical operations with non-numeric values.

**Solution**: Use type coercion or parseInt/parseFloat functions to convert the values to numbers before performing mathematical operations.
```js
// example
let x = '10';
let y = 20;
console.log(x * y); // 200

// or
let x = '10';
let y = 20;
console.log(parseInt(x) * y); // 200
 ```
 
 ### 4. Infinite loop
**Cause**: This error occurs when a loop doesn't have a proper termination condition.

**Solution**: Make sure the loop has a proper termination condition that eventually evaluates to false.
```js
// example
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

### 5. Incorrect URL or API endpoint

**Cause**: This error occurs when the URL or API endpoint being accessed is incorrect or doesn't exist.

**Solution**: Check the URL or API endpoint for typos or spelling errors, and make sure it's a valid endpoint.

```js
// example
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```
