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
