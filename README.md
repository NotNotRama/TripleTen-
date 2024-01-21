# TripleTen Assignment 

## Insights into Junior Full-Stack Developer Skill Requirements

How much knowledge on these areas depends on the company you'll be interviewing with. FAANG companies, even for frontend positions, tend to emphasize algorithms to filter through the large number of candidates they receive. For companies outside the very top, the emphasis on knowledge of algorithms and data structures tends to diminish, as more practical knowledge is required, specially at startups outside big tech hubs (like the Bay Area). 

Regardless, acquiring a foundational understanding of algorithms is recommended. For instance, understanding Big O notation, even if not applied daily, proves useful in writing efficient code.

Concerning testing, while having a test suite in any codebase is important, its significance may be lower for junior roles, especially those requiring no previous experience. However, encouraging a basic understanding of testing, such as unit testing, is advisable.

TypeScript, on the other hand, has become the standard these days compared to how it was years ago and is required in almost every job listing. And with good reason since it helps you catch possible bugs from the get go. 


## Introduction to TypeScript

Considering its significance and widespread use today, let's delve into a brief introduction to TypeScript, explore its advantages, and hopefully, inspire you to consider using it in your future projects.

Before the advent of TypeScript (TS), JavaScript (JS) allowed you to define variables like this:

```js
let a = 5;
```
And functions like this:

```js
function sum(a, b) {
  return a + b;
}
```

JS is a dynamically typed language, meaning a variable can initially hold one type (e.g., a number) and later be assigned another type (e.g., a string). While JS is flexible and beginner-friendly, it comes at the cost of uncertainty in your code.

Let's take the sum function as an example. If you call it with `sum("2", "2")`, JS will concatenate the strings instead of performing a numerical sum. This flexibility can lead to unexpected bugs, especially in larger codebases.

This is where TypeScript comes into play.

Let's modify our sum function:

```js
function sum(a: number, b: number) {
	return a + b;
}
```

Here, we added the type number to our parameters. Now, you can only pass arguments of type number. If you attempt to call `sum("2", "2")`, TypeScript will catch it and raise an error, helping you catch bugs early in development.

You can even be more explicit by defining the return type:

```js
function sum(a: number, b: number): number {
	return a + b;
}
```
This ensures that whatever is returned from this function must be of type number.

Beyond bug-catching, TypeScript enhances code readability. You can define custom types with interfaces or types:

```ts
interface User {
	firstName: string;
	lastName: string;
	age: number;
}

const user: User = {
	firstName: "John",
	lastName: "Doe",
	age: 30
};
```
By using interfaces or types, you gain insights into the structure of objects. For example:

```js
function greetUser(user: User): string {
    return "Hello, " + user.firstName + " " + user.lastName + "!";
}
```
By looking at it, you know that the function `greetUser` expects a parameter of type User and will return a string.

Another advantage, at least if you're using Visual Studio Code (VSC), is the helpful autocompletion. Typing `user.` will show you the available options or keys (`firstName`, `lastName`, and `age`) for that object.

As a last piece of advice, I'd recommend the usage of [Pretty TypeScript Errors](https://github.com/yoavbls/pretty-ts-errors) as it makes the TS errors in VSC much more readable.

