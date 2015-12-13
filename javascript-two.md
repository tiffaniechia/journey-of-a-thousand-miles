## Javascript II -  Functions

What are functions? You can think of functions as little self contained programs. For example this is a tiny program that returns one plus one.

```javascript
function onePlusOne() {
  var total = 1 + 1;
  return total;
}
```

Functions also take in parameters which makes them more extendable. For example the below takes in parameter x and y, and returns the total.

```javascript
function add(x, y) {
  var total = x + y;
  return total;
}
```

To use the add() function all I do is call it like that:

```javascript
add(1,2);
```
where 1 is x, and 2 is y. The function will then return 3!

You can imagine how far and wide functions can take us! Applications are made out of many tiny functions. Think of it like a factory production line, you have factory workers each specifically does one job and outputs a specific bit of a product, and passes it on to the next worker in the factory line. An application is something like that, but instead of factory workers, we have functions.

Functions are usually declared with 'function' followed by the name of the function, and the parenthesis that will take in optional parameters. You will then close the algorithm in '{}' and return what you want your function to output.


```javascript
function nameOfFunction(optionalParameters, youShouldLeaveItBlankIfYouDoNotHaveAny) {
  #enclose your algorithm here between the squiggly brackets
  #you will need to return something.
  #What you 'return' is what your function will output.
  return x;
}
```
When the function gets to the return statement, it will exit the function.  If no return statement is used (or an empty return with no value), it will return undefined. This is very important! There are times where you need a function to manipulate data and not output anything - but if not, remember your return statements!

Functions let you hold your little program and use it only when you need it. Remember the 'add' function you wrote previously? The function will not be executed until you call 'add(1,2)'. It also means you can write a function once, but use it more than once! You have to call a function before it is executed!


### Your objective for this section:
- [ ] [Go through Code Academy Functions section](https://www.codecademy.com/courses/javascript-beginner-en-6LzGd/0/1?curriculum_id=506324b3a7dffd00020bf661)
- [ ] [Build rock paper scissors with your new found knowledge!](https://www.codecademy.com/courses/javascript-beginner-en-Bthev-mskY8/0/1?curriculum_id=506324b3a7dffd00020bf661)
- [ ] Make sure you understand the concept of global and local scopes!

#### Test:
Now that you know variables, conditions, and functions, let's attempt to write the [fizzbuzz game](https://en.wikipedia.org/wiki/Fizz_buzz)!
Fizz Buzz is a counting game where all multiples of 3 is fizz, all multiples of 5 is buzz, all multiples of 3 and 5 is fizzbuzz. SO it will go like this: 1, 2, fizz, 4, buzz, fizz, 7, 8, fizz, buzz, 11, fizz, 13, 14, fizzbuzz.

write a program where I can input a number, and it will give the correct output.

```javascript
play(1) #will output 1
play(3) #will output fizz
play(5) #will output buzz
play(15) #will output fizzbuzz
```

Write the program and commit it to GitHub under a new repository named GitHub!

### For giggles:
- [ ][Learn Javascript with Javascript for cats, a fun non-indepth way of going through javascript.](http://jsforcats.com/)

#### If you would like extra practice:
Peer into available functions for different data types:
You can write your own methods to create more complex logic (or build on other functions), but there are prewritten functions (or methods) that come inbuilt with Javascript and it's respective data types so you don't have to reinvent the wheel and re-write the logic!
- [ ] [Explore what you can do to transform String data types](http://www.w3schools.com/js/js_string_methods.asp)
- [ ] [Explore what you can do to transform Number data types](http://www.w3schools.com/js/js_number_methods.asp)
- [ ] [Explore what you can do to transform boolean data types](http://www.w3schools.com/js/js_comparisons.asp)



#### Hint for test (one of simpler the ways!):  
```javascript
function play(input) {
  if (divisibleBy15(input)) {
    return 'fizzbuzz';
  };
  if (divisibleBy3(input)) {
    return 'fizz'
  };
  if (divisibleBy5(input)) {
    return 'buzz'
  };
  return input;
}

function divisibleBy15(input) {
  var divisible = input % 15 == 0;
  return divisible;
}

function divisibleBy5(input) {
  var divisible = input % 5 == 0;
  return divisible;
}

function divisibleBy3(input) {
  var divisible = input % 3 == 0;
  return divisible;
}

```
