## Javascript III - If/Else, Switches, Logical Operators, and understanding control flow

What are computer programs if not a set of operations? We learnt the power of simple if else statements from the previous tutorials.

Along with using logic statements, it is crucial to understand how your code is being processed (the order in which it is being evaluated), this will allow us to write applications that work and understand why bugs come up. Javascript evaluates step by step (line by line). Take for example the fizzbuzz test from the previous tutorial:

```javascript
function play(input) {
  if (input % 15 == 0) {
    return 'fizzbuzz';
  };
  if (input % 3 == 0) {
    return 'fizz'
  };
  if (input % 5 == 0) {
    return 'buzz'
  };
  return input;
}

console.log(play(15)) //returns fizzbuzz
console.log(play(5)) //returns buzz
console.log(play(3)) //returns fizz
console.log(play(7)) //returns 7

```

if we switched the position of the if statement of (input % 15 ==0) and (input % 3 == 0), we will get a bug where play(15) will never return fizzbuzz

```javascript
function play(input) {
  if (input % 3 == 0) {
    return 'fizz';
  };
  if (input % 15 == 0) {
    return 'fizzbuzz'
  };
  if (input % 5 == 0) {
    return 'buzz'
  };
  return input;
}

console.log(play(15)) //returns fizz instead of fizzbuzz

```

This is because if we run it step by step, because 15 is also divisible by 3, it will enter the first if statement and return fizz, and exit the function altogether, hence never reaching the second if statement! This is why control flow is so important, and know how your code steps along is crucial.

Now that you have understood the important of control flow, we can use the great powers of logical operators! It helps us moderate complex logic decisions that we might need.

```javascript
false && false //false
true && false //returns false
false && true //returns false
true && true //returns true

false ||  false // returns false
true || false //returns true
false || true // returns true
true || true //returns true
```

### Your objective for this section:
- [ ] [Go through Code Academy Control Flow section](https://www.codecademy.com/courses/javascript-beginner-en-qDwp0/2/2?curriculum_id=506324b3a7dffd00020bf661)
- [ ] [Make a choose your adventure game](https://www.codecademy.com/courses/javascript-beginner-en-ZA2rb/0/1?curriculum_id=506324b3a7dffd00020bf661)

### If you would like extra practice:
- [ ] [Learn about ternary operators](https://msdn.microsoft.com/en-us/library/be21c7hw.aspx)
```javascript
conditionToBeEvaluated ? willExecuteIfTrue : willExecuteIfFalse
```
- [ ] [Mozilla switch statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch)
