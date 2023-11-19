# Answers

## Section 1

#### 1.	JavaScript and its Historical Development
  -	JavaScript is a programming language mainly used in web browsers. It emerged in 1995 under the name "Mocha" by Netscape, later renamed "LiveScript," and ultimately became known as "JavaScript." It was standardized by ECMAScript. Evolving over time, it enabled the development of dynamic and interactive web applications. Key milestones include the introduction of AJAX for asynchronous data exchange and updates to the ECMAScript standards. In its modern form, JavaScript, with ES6 and later versions, supports both client and server-side development, making it a versatile language. With these features, it forms the foundation of web development.
#### 2.	Difference Between Java and JavaScript
   - Java is a general-purpose programming language that can be used in various application types, whereas JavaScript is a scripting language specifically designed to run in web browsers. It is used to make web pages interactive. Despite the similarity in names, there are many differences, including syntax, use cases, and execution environments.
#### 3.	Data Types in JavaScript
- Primitives
	- String : Represents textual data.
	- Number : Represents numerical data.
	- Boolean : Represents logical values.
	- Symbol: Represents unique and immutable values.
	- Undefined: The default value for a variable that has not been assigned a value.
	- Null: Represents the absence of a value or an empty value.
- Object and Derived Ones
	- Object : Represents complex data structures.
	- Array : Represents ordered data collections.
	- Function : Represents a reusable block of code.

#### 4.	Difference Between null and undefined
-	`null` signifies that a value has been intentionally set as absent or undefined. On the other hand, `undefined` indicates that a value has not been assigned or is missing.
#### 5.	What is `NaN`
   -	Exactly, NaN stands for "Not-a-Number" and is used in JavaScript to represent the result of a mathematical operation that is undefined or unrepresentable as a real number. It typically occurs when you attempt to perform an invalid operation, such as dividing zero by zero or attempting to parse a non-numeric string.
#### 6.	Ways to Add Comments in JavaScript
-	Signle-Line Comment
	```javascript
 
	// This is a single-line comment.
 
	```
-	Multi-Line Comment
	```javascript
		/* 
	This
	is
	a
	multi-line
	comment.
	*/

	```
#### 7.	Global Variable in JavaScript
-	A global variable is a variable that can be accessed from anywhere in the program and is valid throughout the entire program.
#### 8.	`this` Keyword in JavaScript
   -	The `this` keyword, when used inside a JavaScript function, represents the current context. The context specifies in which object or scope the function is running. By using `this`, you can access the object or scope in which the function is being executed.
#### 9.	Difference Between `==` and `===`
	-	`==` operator only compares values and performs type coercion:
	```
	'5' == 5 // true, because type coercion is performed, and values become equal.
	```
	-	`===` operator checks whether the values and data types are both equal, without performing type coercion:
	```
	'5' === 5 // false, because data types are different.
	```
#### 10.	Difference Between `let`, `var`, and `const`
| Feature | `let`| `var` | `const` |
| ------- | ---- | ----- | ------- |
| Scope | block | function | block |
| Redeclaration | No | Yes | No |
| Reassignment | Yes | Yes | No |
| Mandatory Initialization  | No | No | Yes |

#### 11.	Differences Between Arrow Function and Regular Function
- Arrow functions have a shorter syntax.
- Arrow functions do not have their own `this` context; they inherit the context in which they are defined, whereas regular functions depend on the context in which they are called.
- Arrow functions cannot use the `arguments` object; in regular functions, `arguments` contains the arguments passed to the function.
- If an arrow function returns a single expression, curly braces and a `return` statement are not required.
#### 12.	Defining Variables Inside a Switch Block
- If the variable will only exist within the switch block, it can be defined using `let` or `const` inside the case blocks.
- If the variable needs to be reassigned outside the switch block, it should be declared using `let` or `const` outside the block.
#### 13. Pure Function
   -	Always produces the same output for the same input.
	 -	Does not make any changes outside itself; it has no side effects.
	 -	Depends on inputs and is not dependent on external factors.
	 -	Easier to test and understand.
#### 14. Rest Operator
   -	The rest operator is used to gather variable numbers of arguments in function parameters or elements in an array. It is typically denoted by three dots (...) and is useful for combining values.
#### 15. Object Destructuring
   -	Object destructuring is the process of extracting properties from an object and assigning the values of those properties to variables. This enhances the readability and organization of the code.
```javascript
const person = {
  firstName: 'Metehan',
  lastName: 'Karaşahinoğlu',
  age: 25,
}
const { firstName, lastName, age } = person
console.log(firstName) // 'Metehan'
console.log(lastName)  // 'Karaşahinoğlu'
console.log(age)       // 25
```
#### 16. Creating a 2-Element Object in 6 Different Ways
```javascript
const obj1 = { key1: 'value1', key2: 'value2' }
```
```javascript
const obj2 = new Object()
obj2.key1 = 'value1'
obj2.key2 = 'value2'
```
```javascript
const { key1, key2 } = { key1: 'value1', key2: 'value2' }
const obj3 = { key1, key2 }
```
```javascript
const objPrototype = { key1: 'value1', key2: 'value2' }
const obj4 = Object.create(objPrototype)
```
```javascript
const obj5 = Object.assign({}, { key1: 'value1', key2: 'value2' })
```
```javascript
const jsonStr = '{"key1": "value1", "key2": "value2"}'
const obj6 = JSON.parse(jsonStr)
```
#### 17. Create a new object using two different loop methods  with the character length of key and value of a 2-element object
```javascript
const mainObject = {
    key1: "valueFirst",
    key2: "valueSecond",
  }
  
  const newObject = {}
  
  for (const key in mainObject) {
    const value = mainObject[key]
    newObject[key] = value.length+key.length;
  }

  console.log(newObject)  // { key1: 14, key2: 15 }
```
```javascript
const mainObject = {
    key1: "valueFirst",
    key2: "valueSecond",
  }

const newObject = {}

for (let key in mainObject) {
  const value = mainObject[key]
  newObject[key] = value.length+key.length
}

console.log(newObject); // { key1: 14, key2: 15 }
```
#### 18. Difference Between Cookie, Local Storage, and Session Storage
| Feature | `cookie`| `local storage` | `session storage` |
| ------- | ---- | ----- | ------- |
| Storage Scope | Stores data between the browser and the server. |	Stores data only on the client side in the browser.|	Stores data only for the duration of the session in the browser.|
| Size Limit | 4KB | 5MB | 5MB |
| Data Transmission |Automatically sent with HTTP requests.	|Not sent automatically, needs to be done manually.	|Not sent automatically, needs to be done manually.|
| Persistence | Can be stored for a defined period (usually a few weeks) until manually cleared by the user.|	Persists until manually cleared by the user.|	Cleared when the browser window/session is closed.|
| Access | Accessible only on specified domains, paths, and with certain security features on pages.|	Accessible only on the specified domain.|	Accessible only on the specified domain.|
| Use Case | Used for various application scenarios such as session management, preferences, tracking, etc.|	Primarily used for persistent data storage.|	Used for temporary data storage during the page session.|
#### 19. Asynchronous vs Synchronous Operations
   - Synchronous Operation
		-	Code runs sequentially; one operation must finish before the next one starts.
		-	Operations can block each other.
   - Asynchronous Operation
		-	Code runs sequentially, but some operations may wait for a certain period.
		-	Operations do not have to wait for each other.
#### 20. Promise in JavaScript
   - Promise is an object in JavaScript used to manage asynchronous operations. It represents operations to be performed when a process is completed or fails.
   - Why Do We Need It:
		- Managing Asynchronous Operations: Asynchronous operations, such as API calls or file reading/writing, can take time. Promise allows us to handle such operations more efficiently.
		
		- Reducing Callback Hell: Used to prevent the callback hell situation that arises when multiple asynchronous operations are nested inside each other.
		
		- Error Handling: Promise enables effective handling of errors in asynchronous operations. Error management can be easily done using the .catch() block.

## Section 2

### Section 2.1

```javascript
// - 1 -
let dolap = ["Shirt", "Pant", "TShirt"];
dolap.pop()
console.log(dolap)
```

```javascript
// - 2 -
let dolap = ["Shirt", "Pant", "TShirt"];
dolap.splice(0,1,"Hat")
console.log(dolap)
```

```javascript
// - 3 -
let dolap = ["Shirt", "Pant", "TShirt"];
let result = Array.isArray(dolap)
console.log(result)
```

```javascript
// - 4 -
let dolap = ["Shirt", "Pant", "TShirt"];
let result1= dolap.includes("Pant")
let result2= dolap.some(e=> e==="Pant")
let result3= dolap.find(e=> e==="Pant") ==="Pant" ? true:false
console.log(result1,result2,result3)
```

```javascript
// - 5 -
let dolap = ["Shirt", "Pant", "TShirt"];
let sum=0
dolap.forEach(e=> sum+=e.length)
console.log(sum)

```

```javascript
// - 6 -
let dolap = ["Shirt", "Pant", "TShirt"];
let newVar1=""
dolap.forEach(e=> newVar1+=e.toUpperCase())
let newVar2=""
dolap.map(e=> newVar2+=e.toUpperCase())
let newVar3=dolap.join("").toUpperCase()
console.log(newVar1,"\n",newVar2,"\n",newVar3)
```

```javascript
// - 7 -
let dolap = ["Shirt", "Pant", "TShirt"];
let dolapObject= Object.fromEntries(dolap.map((item,index)=>[index,item]))
console.log(dolapObject)
```

### Section 2.2

```javascript
// - 1 -
const arr=[1,2,3,4,5,6,7,7,,8,6,10];
const repeated= arr.filter((item,index)=> arr.indexOf(item)!==index)
```

```javascript
// - 2 -
const arr=[1,2,3,4,5,6,7,7,,8,6,10];
const repeatesDeleted= arr.filter((item,index)=> arr.indexOf(item)===index)
console.log(repeatesDeleted)
```

```javascript
// - 3 -
const arr=[1,2,3,4,5,6,7,7,,8,6,10];
const lowestNumber=arr.sort().slice(0,1)[0]
const highestNumber=arr.sort((a,b)=> b-a).slice(0,1)[0]
console.log(lowestNumber,highestNumber)
```
### Section 2.3
