# Difference between var, let, and const keywords in JavaScript

In JavaScript, there are three keywords used in declaring a variable, these are the var, let, and const keywords. In this article, we will be discussing the major differences and when to use them. If you stick around till the end, you will find out which is the most preferred and safest to use.

## var keyword
Before the arrival of ES6(ECMAScript version 6) in 2015, one of the oldest ways of declaring a variable was with the use of the **var** keyword. Although, the usage of the var keyword was problematic to work with and was prone to bug issues. 

Here are some of the ways to declare a variable using the var keyword with regard to its **scope**.

## What is a variable scope?
A **scope** is the availability of variables either globally or locally. 

- Globally, in the sense that the variable can be seen everywhere and used within any part of the script, likewise, within a function.

- Locally means that the variable can only be used and accessed within a given function or block scope.

Let's look at some examples.

**Example 1**

Variables can be re-declared multiple times using the var keyword and can still be updated after re-declaration.

```
<script>

   var name = 'John'; // First declaration

   var name = 'Peter'; // Variable re-declared 

   var name = 'Sarah'; // Variable re-declared one more time

   name = 'Jessica'; // Variable updated and assigned a new value

   console.log(name); // Jessica

</script>
```

**Example 2**

When a variable is declared and initialized globally, it means that it has a global scope and can be accessed anywhere in the script.

```
<script>

   var number = 5;

   function func() {
      console.log(number);
   }
   func(); // 5 (within the function)
   console.log(number); // 5 (outside the function)

</script>
```

**Example 3**

When a variable is used before it has been declared and assigned a value, it results in undefined.

```
<script>

   console.log(x); // undefined
   var x = 2;

   // Results in undefined

</script>
```

**Example 4**

When a variable is declared and assigned within a function, it can not be accessed outside the function. This is called **function scoped** and the variable is regarded as a **local variable** within the function.

```
<script>

   function aFunc() {
     var numb = 4;
     console.log(numb); // numb can be accessed anywhere within the function
   }
   aFunc(); // 4
   console.log(numb); // Error! numb not defined (can't access the variable numb, outisde the function)

</script>
```

## let keyword

With the arrival of ES6 in 2015, the **let** keyword was introduced. Most developers now make use of the let keyword for declaring and assigning a variable.

The let keyword uses a block scope, which means that a variable declared within a particular block can not be accessed outside that block.

A block is when an opening curly brace { and a closing curly brace } enclose a statement or a group of statements. 

Let's look at some examples of declaring variables using the let keyword.

**Example 1**

The variable defined using the let keyword is both block-scoped and function scope.

```
<script>
   let x = 5;
   function theFunc() {
      if(x === 5) {
         let y = 10;
         console.log(y); // 10
      }
      console.log(y); // Error! y is defined within the "if" block
   }
   theFunc(); // 10 
   console.log(x); // 5 (global variable in a global scope)
   console.log(y); // Error! Can't be accessed outside the "if" block.

</script>

```
**Example 2**

Using the let keyword when declaring variables, variables can have the same name in different scopes.

```
<script>
   let apples = 5; // global scope
   function funcA() {
      if(true) {
         let apples = 2; // function scope
         console.log(apples); // 2 not 5 (due to variable shadowing)
      }
   }
   funcA(); // 2
   console.log(apples); // 5 (Uses the global variable that can be accessed anywhere)
</script>

```
### Variable shadowing 

You might be wondering, what variable shadowing is. Well, it is when two variables have the same name in two different scopes i.e a global scope, and another within a block scope e.g a function block scope or an "if" block. With variables having the same name, the block scope shadows the global scope. 

In other words, the variable within a block is of higher precedence compared to the global scope. Outside the block, the global variable is used.

**Example 3** 

Unlike the var keyword which can be used to re-declare a variable multiple times, this can not be done using the let keyword.

```
<script>
   let i = 5;
   let i = 10; // Results in an Error

   i = 10; // This is allowed ("i" has been updated.)

   console.log(i); // 10
</script>

```

**Example 4**

Unlike the var keyword that returns undefined when a variable is used before it is declared and defined, doing that using the let keyword results in an error.

```
<script>
   console.log(z); // Error! Cannot access z before initialization 
   let z = 20; 
</script>

```

## const keyword

The **const** keyword is similar to the let keyword in terms of properties. Although, there are differences between the two. With the const keyword, the value of the variable will always remain constant and cannot be updated once declared and assigned a value.

You can declare a variable using the let keyword without assigning a value to it, but with the const keyword, it throws an error.

**Example 1**

Variables cannot be updated when declared and defined with the const keyword

```
<script>
   const dateOfBirth = '17/09/2002';
   dateOfBirth = '14/05/2003'; // Error! Assignment to constant variable 
</script>

```

**Example 2**

A variable cannot be declared without assigning it a value.

```
<script>
    const PI;  //Error! Missing initializer in const declaration
    PI = 3.14;
</script>

```

**Example 3** 

The property names of a constant object cannot be changed but the property values of the const object can be accessed and updated to a new value.

```
<script>
    const pricesOfItems = {
          bread: 50,
          milk: 70
     };
     // You can access properties and update their values
     pricesOfItems.bread = 65; // Allowed

     // This is not allowed 
     pricesOfItems = {
          sugar: 50,
          butter: 20
     };

</script>

```

## Conclusion 
In this tutorial, we learned about the differences between the variables keywords used in declaring a variable using var, let, and const. By now we can tell the differences between all keywords and know when to use them.

**Important Note** - it is advised to stick with declaring variables with either the let and const keywords, especially the **const** keyword if you wouldn't like to mistakenly alter or update the values of the variable that has been declared and assigned a constant unchangeable value. 

The var keyword is no more in use by most developers. Although you can still find them in an old code base. It is good to know but avoid them by all means because they are prone to bug.





