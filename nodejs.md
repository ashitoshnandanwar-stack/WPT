# Express

## MiddleWare
Think of middleware as a series of checkpoints that a request passes through before reaching its final destination.
```
What is Middleware?
Middleware is simply a function that has access to:

req (request object) - information coming from the client
res (response object) - what you'll send back to the client
next - a function to pass control to the next middleware
```

### Common Built-in Middleware
```
1. Parse JSON data:
javascriptapp.use(express.json());
// Now you can access req.body in your routes

2. Parse form data:
javascriptapp.use(express.urlencoded({ extended: true }));

3. Serve static files:
javascriptapp.use(express.static('public'));
// Serves files from the 'public' folder

The next() Function
This is crucial! If you don't call next(), the request gets stuck:

// Bad - request hangs!
app.use((req, res, next) => {
  console.log('Stuck here forever!');
  // Forgot to call next()
});

// Good
app.use((req, res, next) => {
  console.log('Moving along...');
  next(); // Passes to next middleware
});
```

💻 Node.js REPL

- REPL = Read–Eval–Print–Loop
- It is an interactive shell to execute JavaScript.
```
Open terminal and type:
node
Then:

> 5 + 3
8

> let a = 10
undefined

> a * 2
20


Use:

Quick testing
Learning JS
Debugging
Exit REPL: .exit


Node.js makes JavaScript a full-stack language – usable both in browser and on server.
```

## Spread operator
```
let arr = [1, 2];
let arr2 = [...arr, 3];


console.log(arr2)
```

## ECMA script 6(ES6)
- ES6 introduced around 15 major features that modernized JavaScript and made it more powerful and easier to use.
- ES6, also known as ECMAScript 2015, is a major update to JavaScript released in 2015. It brought powerful new features that made JavaScript more modern, readable, and efficient for building web applications.
  
| No. | ES6 Feature                                      |
| --- | ------------------------------------------------ |
| 1   | `let` and `const`                                |
| 2   | Arrow Functions `()=>{}`                         |
| 3   | Template Literals `` `Hello ${name}` ``          |
| 4   | Default Parameters                               |
| 5   | Rest & Spread Operator `...`                     |
| 6   | Destructuring (Array/Object)                     |
| 7   | Enhanced Object Literals                         |
| 8   | Classes                                          |
| 9   | Modules (`import` / `export`)                    |
| 10  | Promises                                         |
| 11  | `for...of` loop                                  |
| 12  | Map and Set                                      |
| 13  | Symbols                                          |
| 14  | Generators                                       |
| 15  | New Built-in Methods (Array, String, Math, etc.) |

- ES6 introduced around 15 major features that modernized JavaScript and made it more powerful and easier to use.


<hr>

## 🔄 Asynchronous Programming
- In JavaScript / Node.js, asynchronous programming allows long tasks (like file reading, API calls, DB queries) to run in the background without stopping the main program.
- This keeps the application fast and responsive.

Example (Async task in Node.js):
```
console.log("Start");

setTimeout(() => {
  console.log("Task Done");
}, 2000);

console.log("End");


Output:

Start
End
Task Done


The program does not wait for 2 seconds; it continues executing.
```
📞 Callback Function
- A callback is a function passed as an argument to another function and executed after a task completes.
```
function fetchData(callback) {
  setTimeout(() => {
    callback("Data received");
  }, 1000);
}

fetchData(function(result) {
  console.log(result);
});


Here, function(result) is the callback.
```

## 🤝 Promises in Node.js

- In Node.js, many operations (file read, API call, database access) are asynchronous.
- Earlier, these were handled using callbacks, which often led to: Callback Hell (nested functions), Hard-to-read code, Difficult error handling

- Promises solve these problems by providing a cleaner and more manageable way to handle async tasks.

- A Promise has three states:
```
Pending – operation is in progress
Fulfilled – operation completed successfully
Rejected – operation failed
```
Basic syntax:
```
let p = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Task completed");
  } else {
    reject("Task failed");
  }
});

p.then(result => {
  console.log(result);
}).catch(error => {
  console.log(error);
});
```
