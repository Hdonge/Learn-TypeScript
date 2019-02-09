# Learn TypeScript in two hours

TypeScript is the **typed superset** of the JavaScript that compiles to plain Javascript. Nowadays typescript is becoming very popular in frontend development frameworks due to various key fetaures over JavaScript. TypeScript originated from the shortcomings of the JavaScript development challenges with dealing with complex JavaScript code led to demand for custom tooling to ease developing of components in the language.

TypeScript is an opensource programming langauge developed and maintained by Microsoft. TypeScript was made public in Oct 2012. **Anders Hejlsberg**, lead architect of C# worked on the development of TypeScript.


## JavaScript vs EcmaScript vs TypeScript

Developers often seem confused between EcmaScript and TypeScript due to latest Es6 features adopted by Javascript. 

**Javascript:** JavaScript (JS) is a lightweight, **interpreted or JIT compiled programming language**, most well-known as the scripting language for Web pages. Many non-browser environments also use it, such as node.js. JS is a prototype-based, weakly typed, multi-paradigm, dynamic scripting language, supporting object-oriented, imperative, and declarative (e.g. functional programming) styles.
JavaScript  to the ECMAScript specification. Browsers understand only JavaScript as programming language.

**EcmaScript:** ECMAScript (or ES) is a trademarked **scripting-language specification** standardized by Ecma International in ECMA-262 and ISO/IEC 16262. It was created to standardize JavaScript, so as to foster multiple independent implementations. JavaScript has remained the best-known implementation of ECMAScript since the standard was first published, with other well-known implementations including JScript and ActionScript. ECMAScript is commonly used for client-side scripting on the World Wide Web, and it is increasingly being used for writing server applications and services using Node.js.

Latest broswers are adapting ES6 standards in which various key fetaures are introduced to JS like classes, Modules, Promises, Block-scoped constructs `let` and `const`, Arrow functions, Multiline strings, Template literals etc.

**TypeScript:** TypeScript has Es6, Es7 and more hence becomes superset. It is **strict statically typed language** also offers key features like Pure Object Orientation, Transpilation and Supporting native Javascript code. Typescript client and server side code can be transpiled into Client-side JavaScript and Server-side Node.Js code later which becomes executable in respective envrironment. It becomes popular amongst developer who come from object oriented backgrounds like C#, Java, C++ who can write simple object oriented code and later it gets transpiled to complex Js to get executed.

**Compiling vs Transpiling:**
**Compiling** is the general term for taking source code written in one language and transforming into another.
**Transpiling** is a specific term for taking source code written in one language and transforming into another language that has a similar level of abstraction. 

So when you compile C#, your method bodies are transformed by the compiler into IL. This cannot be called transpiling because the two languages are very different levels of abstraction.

When you compile TypeScript, it is transformed by the compiler into JavaScript. These are very similar levels of abstraction, so you could call this transpiling.


## TypeScript Environment Setup

The command line TypeScript compilar can be installed as a Node.Js package. 

**Install**
``` 
npm install -g typescript 
```

**Compile**
```
tsc index.ts    //which creates index.js file
```

## TypeScript Key Features

**1. Types:**

TypeScript suports all the javascript datatypes like number, string, boolean, void, null and undefind. With this it also supports user defined datatypes like Arrays, Enums, Classes, Interfaces etc. It also supports Any as a datatype which is the super type of all datatypes.

All can be used as:

```javascript
  let name:string;
  let id:number;
  let details:any;
  
  interface IEmployee {  }
  class Employee implements IEmployee {  }
  
  let employee1:Employee = new Employee();
  let employee2:IEmployee = new Employee();
```

**Strongly/Strict/Statically Typed:**

As introduced Typescript is the stictly typed language so variable declared with one type do not accepts values with other types. In case if values assign with diffrent types then it shows compilation error.


  
