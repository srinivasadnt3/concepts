### Hoisting
function blocks will move up, arrow functions won’t. 
moving declaration to the top and allocating the memory 
compiler allocates memory for variable and function declarations prior to execution of the code.
Conceptually hoisting is often presented as the compiler "splitting variable declaration and initialization, and moving (just) the declarations to the top of the code". This allows variables to appear in code before they are defined. Note however, that any variable initialization in the original code will not happen until the line of code is executed.
```typescript
normalFunction();
function normalFunction(){
    console.log("Normal function code will be moved top and available even before initialization");
}
console.log("only declaration will be moved since its variable-and assigend undefined",arrowFunction);
var arrowFunction = ()=>{
    console.log("arrow function wont move code to top only declaration will move not initialization or code");
}

console.log("normalVar",normalVar);
var normalVar="Declarations will be split and moved to the top and when there is declaration it will allocate memory and assign undefined value";

console.log("blockScopeVar",blockScopeVar);
const blockScopeVar = "It will not be accessed before initialization";

console.log("It will get not defined run time error -> stops the code exicution",arrowFuncitonWithConst);
const arrowFuncitonWithConst = ()=>{
    console.log("Arrow with const");
}
```

### Throttling
[Go to hoisting](#hoisting)
