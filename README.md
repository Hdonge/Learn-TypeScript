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

```javascript
 let temp:string = "foo";
 typeof temp;   //string
 temp = 5;      // compilation error, as can not assign value with number type to string type
 temp = true;   // compilation error, as can not assign value with boolean type to string type
```

But in case of javascript it does not show any compilation error. It changes the type of variable implicitly.

```javascript
let temp;

typeof temp;   //undefined
temp = 1;
typeof temp;   //number
temp = true;.
typeof temp;   //boolean
temp = "bar";.
typeof temp;   //string
```
Hence JavaScript is loosely typed (dynamically typed) language where TypeScript is strongly typed (statically styped) language.

To assign value of any type to any variable use type `any` which acts as super type of all datatypes.

```javascript
let temp: any = "Hello";
console.log(typeof temp);   //string
temp = 9;
console.log(typeof temp);   //number
temp = true;
console.log(typeof temp);   //boolean
```

**2. Classes:**

A class in terms of OOP is a blueprint for creating objects. A class encapsulates data for the object. Typescript gives built in support for this concept called class.

```javascript
   class Employee {
      _name:string;
      _id:number;
      constructor(name:string, id:number){
        this._name = name;
        this._id = id;
      }
   }
```   
Above class can also be written by providing access specifiers in constructor parameters which create class properties implicitly.
```javascript
   class Employee {
      constructor(private name:string, private id:number){
      }
   }
```

Above both code snippets compile into javascript code as below

```javascript
    var Employee = /** @class */ (function () {
        function Employee(name, id) {
            this.name = name;
            this.id = id;
        }
        return Employee;
    }());

```
