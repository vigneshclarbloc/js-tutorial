

# ```1.variable```
 - Variables are named values and can store any type of JavaScript value.

 ```
  var x = 100;
  let y=100;
  const z= 200;

```

# ***```2.scope```***
- Scope refers to the **availability and accessibility  of variables and functions in certain parts of the code**. JavaScript has 3 types of scope:
-  i) ```Block scope```
-  ii)```Function scope or local scope```
-  iii) ```Global scope```

![alt text](https://miro.medium.com/v2/resize:fit:1400/1*KxHwVbB0zhnSVrhrWtT-gg.jpeg)
 #  ***```Block Scope```***
- Before ES6 (2015), JavaScript had only Global Scope and Function Scope.
- ES6 introduced two important new JavaScript keywords: let and const.
- These two keywords provide Block Scope in JavaScript.
- **Variables declared inside a { } block cannot be accessed from outside the block**
### ***```example:1```***
```
{
  let x = 2;
}
// x can NOT be used here
```
### ***```example:2```*** 
```
{
  var x = 2;
}
// x CAN be used here
```
- Variables declared with the ```var``` keyword can NOT have block scope.
- **var** Variables declared inside a { } block can be accessed from outside the block.

# ***```Local scope or functional scope```***
- Variables declared within a JavaScript function, become LOCAL to the function.
- Local variables have Function Scope.
- **it can only be accessed within a function**
 ### ***```example```***
```
// code here can NOT use carName

function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}

// carName can't be accessed here (outside function)
```
# ***```Global scope```***
- Variables declared Globally (outside any function) have Global Scope.
- Global variables can be accessed from anywhere in a JavaScript program.
 ###  ***```example```***
```
let a = "hello"; // global declared
function greet() {
    a = 3;
}
// before the function call
console.log(a);

//after the function call
greet();
console.log(a); // 3
```
# ***```3.Hosting```***
- Hoisting in JavaScript is a behavior in which a **function or a variable can be used before. declaration**
 ###  ***```example```***
```
a = 5; // assign value 
console.log(a);  // use 
var a; //  declare

```
# ***```4.Difference between var,let,const```***
![alt text](https://velog.velcdn.com/images/iha3257/post/f2e15fb2-22d8-4042-bf5c-f6617fd5be57/image.jfif)
 | var | let | const |
| ------ | ------ | -----|
  |The scope of a ```var``` variable is functional scope.. |The scope of a ```let``` variable is block scope. | The scope of a ```const``` variable is block scope.  |
  |It can be ```updated and re-declared``` into the scope.. | It can be updated but cannot be re-declared into the scope.. |  It cannot be updated or re-declared into the scope. |
  |It can be declared without initialization. | It can be declared without initialization. |  It cannot be declared without initialization.. |
  |It can be accessed without initialization as its default value is “undefined”. | It cannot be accessed without initialization otherwise it will give ‘referenceError’. |  It cannot be accessed without initialization, as it cannot be declared without initialization.. |
  |hoisting done, with initializing as ‘default’ value | Hoisting is done, but not initialized (this is the reason for the error when we access the let variable before declaration/initialization |  Hoisting is done, but not initialized (this is the reason for the error when we access the const variable before declaration/initialization |
# ***5.Closure:***         
- a closure gives you access to an ```outer function's scope from an inner function```

 ### ***example***
![alt text](https://miro.medium.com/v2/resize:fit:1400/1*QgJDPOW-e39V-ZzTl2F2gA.png)
```
function init() {
  var name = "Mozilla"; // name is a local variable created by init
  function displayName() {
    // displayName() is the inner function, that forms the closure
    console.log(name); // use variable declared in the parent function
  }
  displayName();
}
init();
```
# ***6.data types*** 
![alt text](https://dotnettrickscloud.blob.core.windows.net/img/javascript/js-datatype.png)

### ***example***
```
// Numbers:
let length = 16;
let weight = 7.5;

//undefined 
let x;       // Now x is undefined

//null 
let x=null;       // Now x is null

// Strings:
let color = "Yellow";
let lastName = "Johnson";

// Booleans
let x = true;
let y = false;

// Object:
const person = {firstName:"John", lastName:"Doe"};

// Array object:
const cars = ["Saab", "Volvo", "BMW"];

// Date object:
const date = new Date("2022-03-25");
```
 #  ***7.How to check data type***     
 ```
  var apple = "apple";
  console.log(typeof apple); // string
  
   var number = 2052021;
  console.log(typeof number); // number
  
 typeof "John"                 // Returns "string"
typeof 3.14                   // Returns "number"
typeof NaN                    // Returns "number"
typeof false                  // Returns "boolean"
typeof [1,2,3,4]              // Returns "object"
typeof {name:'John', age:34}  // Returns "object"
typeof new Date()             // Returns "object"
typeof function () {}         // Returns "function"
typeof myCar                  // Returns "undefined" *
typeof null                   // Returns "object"
 ```
 
 # ***8.type conversion*** 
 - In programming, type conversion is the process of **converting data of one type to another**. For example: converting String data to Number.
 - There are two types of type conversion in JavaScript.
 - ```Implicit Conversion``` - automatic type conversion
 - ```Explicit Conversion``` - manual type conversion
 
***More Details***: https://www.programiz.com/javascript/type-conversion#google_vignette

 # **9.Object:** 
 - JavaScript object is a non-primitive data-type that allows you to **store multiple collections of data**.
 
***how to create object:***
```
//1
const person = {
  firstName: 'testFirstName',
  lastName: 'testLastName'
};

//2
const person = new Object();
person.firstName = 'testFirstName';
person.lastName = 'testLastName';
```

 ***Accessing Object Properties:***
 - You can access the value of a property by using its key.
 
 ```1. Using dot Notation```
 ```
 // syntax objectName.key
 const person = { 
    name: 'John', 
    age: 20, 
};

// accessing property
console.log(person.name); // John
 ```
  ```2. Using bracket Notation```
  ```
   // syntax objectName["propertyName"]
  const person = { 
    name: 'John', 
    age: 20, 
};

// accessing property
console.log(person["name"]); // John
  ```
 ***how to create and access on Nested Objects***
 ```
 // nested object
const student = { 
    name: 'John', 
    age: 20,
    marks: {
        science: 70,
        math: 75
    }
}

// accessing property of student object
console.log(student.marks); // {science: 70, math: 75}

// accessing property of marks object
console.log(student.marks.science); // 70
 ```

  # **10.Object Methods:** 
  ***Object.Create***
 ***More Details***: https://github.com/vignesh222s/js-tutorial/blob/main/image/d8db05d2-3938-43ec-8233-acb5dc3aef2f.jpg?raw=true

  ![alt text]( https://github.com/vignesh222s/js-tutorial/blob/main/image/641a8b5d-aa9e-4f76-a1df-d48c7aa3ca04.jpg?raw=true)
  ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/d8db05d2-3938-43ec-8233-acb5dc3aef2f.jpg?raw=true)
  ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/37695e34-be68-40c9-8757-a4249fad4b2d.jpg?raw=true)
  
   ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/93d16e33-d6c2-4a60-acb1-72f071405afa.jpg?raw=true)
   
  ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/a1639d80-a9c9-484a-8a6b-25b169ded7d0.jpg?raw=true)
  
  ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/ac4591fb-2250-468e-a27c-d5dcc8fc23b1.jpg?raw=true)
    
   # ***event loop:*** 
   - JavaScript is a synchronous single-threaded language, meaning it has one main thread of execution. The Event Loop mechanism allows JavaScript to perform asynchronous operations without blocking the main thread.

The JavaScript engine executes code line by line using a data structure called the Call Stack, which keeps track of function calls. When a function is called, it is added to the stack, and once execution finishes, it is removed from the stack. The Call Stack follows the LIFO (Last In First Out) principle..Async code appears in Call Stack.JavaScript sends the async task to Web APIs

Web APIs are browser-provided features available at runtime that handle asynchronous operations outside the JavaScript engine.

Once the async operation completes, its callback function is placed into the Callback Queue. JavaScript does not directly execute code in  the callbackqueue. It waits until the call stack becomes empty.

The Event Loop continuously monitors the call stack and the callback queue. When the call stack becomes empty, the event loop moves the callback from the queue to the call stack for execution.
   
 ![alt text](https://miro.medium.com/v2/resize:fit:1400/1*0xDGBNrA1WtfSfYY3FJOdw.gif)

  ![alt text](https://www.mwanmobile.com/wp-content/uploads/2023/01/pp9n3grfwgcaqgi30t4e.gif)

  ***example***:
```
function greet() {
    console.log('Hello world');
}
function abc() {
    setTimeout(()=>{
      console.log("later")
    },4000)
}
setTimeout(greet, 3000);
console.log('This message is shown first');

abc();
```

  # ***Synchronous:*** 
  - synchronous means to be in a sequence, i.e. ```every statement of the code gets executed one by one```. So, basically a statement has to wait for the earlier statement to get executed.
  
***example***
```
console.log("first");

console.log("second");

console.log("third");
```
  # ***Asynchronous:*** 
  - Functions running in parallel with other functions are called asynchronous.A good example is JavaScript setTimeout()
  
***example***
```
console.log("first");

setTimeout(()=>{
  console.log("I will finish later!")
},2000)

console.log("third");
```
  # ***setTimeout():*** 
  - The setTimeout() method executes a block of code after the specified time. The method executes the code only once.
  
***example***
```
function greet() {
    console.log('Hello world');
}
function abc() {
    setTimeout(()=>{
      console.log("later")
    },4000)
}
setTimeout(greet, 3000);
console.log('This message is shown first');

abc();
```
  # ***setInterval():*** 
  - The setInterval() method calls a function at specified intervals (in milliseconds).
  - The setInterval() method continues calling the function until ``clearInterval()`` is called, or the window is closed.
  
  ***example***
```
function myTimer() {
  const d = new Date();

  console.log(  d.toLocaleTimeString())
}
setInterval(myTimer, 1000);
```
  # **callback:** 
  - A callback is a function passed as an argument to another function. This technique allows a function to call another function. A callback function can run after another function has finished.
  
 ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/a5515dbe-03ee-4f43-b6c6-fae5b324c5cb.jpg?raw=true)

![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/b5d7c061-21c1-4961-8d3f-f6c6f460b6e1.jpg?raw=true)
***example 1:***
```
//  a few friends have planned for a trip.money ,car and route map is needed for the trip.
// money can be arranged after 5 sec. car can be arranged in 3 sec .route map can be arranged in 
//1 sec .only after we get all this the tour can be successful .

// step 1
const money=(amt,car)=>{
  setTimeout(()=>{
      console.log(" "+amt+" arranged money")
      let step1="stpe1 completed"
      car(step1,RouteMap)
  },6000)

}

// step 2

const car=(step1,RouteMap)=>{
    setTimeout(()=>{
    console.log(step1)
   console.log("received money arranged car with the money")
    let step2="stpe2 completed"
   RouteMap(step2,status)
  
  },4000)
  
}

// step 3

const RouteMap=(step2,status)=>{
  setTimeout(()=>{
       console.log(step2)
       console.log("got route map")
        let step3="stpe3 completed"
       status(step3)
  },3000)
}


const status=(step3)=>{
  setTimeout(()=>{
       console.log(step3)
       console.log("trip,completed successfully!!")
        
  },3000)
}
money(10000,car)
```
***example 2:***
```
const money =(amt,callback)=>{

  setTimeout(()=>{
  console.log(" "+amt+" arranged money")
  let step1="stpe1 complete";
  callback(step1);
  },6000)
  
}

const car=(res1,callback)=>{

  setTimeout(()=>{
   console.log(res1)
   console.log("received money arranged car with the money")
   let step2="stpe2 complete";
  callback(step2)
  },5000)
}

const routeMap =(res2,callback)=>{

  setTimeout(()=>{
      console.log(res2)
    console.log("got route map")
     let step3="stpe3 complete"
  callback(step3)
  },3000)
  
}

const status=(res3)=>{
  setTimeout(()=>{
      console.log(res3)
  console.log("trip,completed successfully!!")
  },2000)
  
}

money(10000, function(res1){
  car(res1,function(res2){
    routeMap(res2,function(res3){
      status(res3)
    })
  })
})

```
***async/await:***
- We use the async keyword with a function to represent that the function is an asynchronous function. The async function returns a promise.
- The await keyword is used inside the async function to wait for the asynchronous operation.
- **async** makes a function return a Promise
- **await** makes a function wait for a Promise

 ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/64648360-9512-427a-a5f6-f6503b2ad7c9.jpg?raw=true)
 
 ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/5c57f044-2625-4479-8f0e-409404d50c6a.jpg?raw=true)
  ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/80937fa0-0314-422a-8950-76ec014aeedc.jpg?raw=true)
   ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/df0ef30e-271c-44d8-8e53-f038b4cc25ad.jpg?raw=true)
  ***example:*** 
 ```
 const money = () => {
  return new Promise((resolve) => {
    setTimeout(() => {
      console.log("Arranged money");
      let step1="step1 complete"
      resolve(step1);
    }, 6000);
  });
};

const car = (msg) => {
  return new Promise((resolve) => {
    setTimeout(() => {
      console.log(msg)
      console.log("Received money, arranged car with the money");
      resolve();
    }, 5000);
  });
};

const routeMap = () => {
  return new Promise((resolve) => {
    setTimeout(() => {
      console.log("Got route map");
      resolve();
    }, 4000);
  });
};

const status = () => {
  return new Promise((resolve) => {
    setTimeout(() => {
      console.log("Trip completed successfully!!");
      resolve();
    }, 3000);
  });
};

const res = async () => {
  const result=await money();
  await car(result);
  await routeMap();
  await status();
};

res();
 ```
 ***Promises:***
 - A Promise is a JavaScript object that links producing code and consuming code.
 - ***Producing code*** is code that can take some time.
 - ***Consuming code*** is code that must wait for the result.
 
  ***why used:***
- In JavaScript, a promise is a good way to handle asynchronous operations. It is used to find out if the asynchronous operation is successfully completed or not.
- A promise may have one of three states.
- Pending
- Fulfilled
- Rejected
- A promise starts in a pending state. That means the process is not complete. If the operation is successful, the process ends in a fulfilled state. And, if an error occurs, the process ends in a rejected state.

***Create a Promise***
```
let promise = new Promise(function(resolve, reject){
     //do something
});
```
***More Details***: https://www.programiz.com/javascript/promise

 ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/c5e21695-a5c0-494e-a1b1-d9e1dbba471e.jpg?raw=true)
 ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/91a4f29e-f546-44ae-a6d3-bcd4bf57dfcd.jpg?raw=true)
 ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/4c9602ec-961b-4f4a-8edf-1ef48ed22708.jpg?raw=true)
 
***Promise.then():***
- The then() method returns a Promise. It takes up to two arguments: callback functions for the success and failure cases of the Promise.
```
const promise1 = new Promise((resolve, reject) => {
  resolve('Success!');
});
promise1.then((value) => {
  console.log(value);
  // expected output: "Success!"
}, (error) => {
  console.log( error);
});
```
***Promise.catch()::***

  ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/f5d53ea3-d506-40d8-9dac-c46d84f011db.jpg?raw=true)
  
  ***Promises Vs Callback:***
  
  ![alt text](https://github.com/vignesh222s/js-tutorial/blob/main/image/6d9b4d1c-beaf-44a4-9533-1688c5f2755d.jpg?raw=true)
  
  ***Promise.finally():***
  - The finally() method returns a Promise. When the promise is settled, the specified callback function is executed. This provides a way for code to be run irrespective of promise settlement. A finally callback will not receive any argument, since there is no way of determining if the promise was fulfilled or rejected.
  ```
  const promise1 = Promise.reject("Rejecting Promise");
promise1
  .then(value => {
    console.log(value)
  })
  .catch(err => {
    console.log(err)
  })
  .finally(() => {
    console.log("completed promise")
  });
> "Rejecting Promise"
> "completed promise"
  ```
  ***examples***
  ```
   const money = () => {
   return new Promise((resolve) => {
    setTimeout(() => {
      console.log("Arranged money");
      let step1 = "step1 complete";
       resolve(step1);
    }, 6000);
   });
 };

 const car = (msg) => {
   return new Promise((resolve) => {
   setTimeout(() => {
      console.log(msg);
       console.log("Received money, arranged car with the money");
     resolve();
    }, 5000);
  });
};

 const routeMap = () => {
  return new Promise((resolve) => {
   setTimeout(() => {
    console.log("Got route map");
    resolve();
  }, 4000);
 });
 };
 const status = () => {
  return new Promise((resolve) => {
   setTimeout(() => {
     console.log("Trip completed successfully!!");
      resolve();
   }, 3000);
   });
 };


 money()
   .then((result) => {
     return car(result);
  })
 .then(() => {
  return routeMap();
 })
   .then(() => {
    return status();
   })
  .catch((error) => {
    console.error("An error occurred:", error);
   });
  ```
  ***Promises Methods:***
  
  ***1.Promise.all():***
  - ``waits for all promises to be resolved or any one to be rejected.``
  - Promise.all() method takes an array of promises and returns a single promise, which is either resolved or rejected based on any iterable promise. It resolves if all the promises inside the array resolve and reject if any of the promises reject.

***example***
```
const promise1 = Promise.resolve("hello world");
const promise2 = "Promise 2";
const promise3 = new Promise((resolve, reject) => {
  setTimeout(resolve, 100, 'foo');
});
Promise.all([promise1, promise2, promise3]).then((values) => {
  console.log(values);
});
// expected output: Array ["hello world", "Promise 2", "foo"]
```
***example2***
```
const pro1 = new Promise((resolve, reject) => {
  setTimeout(() => resolve("one"), 1000);
});

const pro2 = new Promise((resolve, reject) => {
  setTimeout(() => resolve("two"), 2000);
});

const pro3 = new Promise((resolve, reject) => {
  setTimeout(() => reject("rejected"), 3000);
});

Promise.all([pro1, pro2, pro3])
  .then((values) => {
    console.log(values);
  })
  .catch((error) => {
    console.log(error);
  });
  //expected output: rejected
```
 ***2.Promise.any():***
 - ```Returns the promise value as soon as any one of the promises is fulfilled```
 
***example***
```
const SlowlyDone = new Promise((resolve, reject) => {
  setTimeout(resolve, 500, "Done slowly");
}); //resolves after 500ms

const QuicklyDone = new Promise((resolve, reject) => {
  setTimeout(resolve, 100, "Done quickly");
}); //resolves after 100ms

const Rejection = new Promise((resolve, reject) => {
  setTimeout(reject, 100, "Rejected"); //always rejected
});

Promise.any([SlowlyDone, QuicklyDone, Rejection])
  .then((value) => {
    console.log(value);
    //  QuicklyDone fulfils first
  })
  .catch((err) => {
    console.log(err);
  });
```
 ***3.Promise.race():***
 - ```Wait until any of the promises is resolved or rejected```
 
 ***example***
```
const pro1 = new Promise((resolve, reject) => {
  setTimeout(() => resolve("one"), 200);
});

const pro2 = new Promise((resolve, reject) => {
  setTimeout(() => resolve("two"), 100);
});

Promise.race([pro1, pro2])
  .then((response) => {
    console.log(response); //output: two
  })
  .catch((err) => {
    console.log(err);
  });

const pro3 = new Promise((resolve, reject) => {
  setTimeout(() => reject("rejected"), 300);
});

const pro4 = new Promise((resolve, reject) => {
  setTimeout(() => resolve("four"), 400);
});

Promise.race([pro3, pro4])
  .then((response) => {
    console.log(response);
  })
  .catch((err) => {
    console.log(err);
  }); //output: rejected

```
***4.Promise.allSettled():***
- ```Waits until all promises are either resolved or rejected```

***example:***
```
let first_promise = Promise.resolve(200);
 
let second_promise = Promise.reject("Rejected Promise");
 
let third_promise = new Promise((resolve, reject) => {
    setTimeout(() => resolve(500), 100)
});
 
let result =
    Promise.allSettled([first_promise, second_promise, third_promise]);
result.then((value) => console.log(value));
 
```
