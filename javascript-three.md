## Javascript III -  For loops & While loops, and Arrays

What are loops and what are they good for? We've been learning how to create variables and functions. But what if you want to execute a function 10 times? You could conceivably write it 10 times, but what if you needed to execute it 20 times? Or 200 times? You don't want to write it 200 times do you?

Here is where loops come in. You make the function run in a loop while you sit back and wait for it to do it's magic.

```javascript

console.log('you are beautiful!');
console.log('you are beautiful!');
console.log('you are beautiful!');
console.log('you are beautiful!');
console.log('you are beautiful!');

#or you could execute a loop

for ( var i = 0; i<=4; i++ ) {
  console.log('you are beautiful!');
}

// the loop has the same effect as calling it 5 times. (0,1,2,3,4 = 5 times)
// variable 'i' is simply a counter that says, declare it as 0 (var i = 0),
// increment by 1 variable i (i++) every time the loop runs,
// and while variable i is less than or equals to 5 (i<=5), execute whatever is inside the loop.


// so variable i = 0 is less than 5, will execute it once,
// var i = 1 is less than 5 so it will execute it again,
// var i = 5 still fulfills <=5 so it will execute again
// var i = 6 does not fulfill the requirement so the loop exits
```

You can imagine how many times you can execute a function this way! Just by tweak the numbers you can make the computer say you're beautiful all day long!

You can also make the Loop count downwards

``` javascript
for ( var i = 4;  i>=0; i-- ) {
  console.log('you are beautiful!');
}
```

There are also while loops, which works the same as the english language. So, for example you would normally say, While it rains, I want to stay in. Or better yet, a donut counter that counts the number of donuts you ate.


```javascript
var donutCounter=0
while (donutCounter <= 12) {
    console.log('I have eaten ' + donutCounter + ' donuts')
    donutCounter++;
}
```

I imagine you have grasped the concept of counting loops. Loops can also help you to search for things. Like searching for a needle in the haystack. So for example:

```javascript
while (item != 'needle') {
    keepSearchingTheHayStack();
}
```

Just imagine the possibilities it loops can bring!

Along with Loops comes the concept of Arrays. In the most simplistic term, an Array is simply a list. Because sometimes we have a list of things we need to loop through

```javascript
var groceryListArray = ['cupcake', 'chocolate', 'rainbows', 'cookies'];

groceryListArray[0] //will return 'cupcake'
groceryListArray[1] //will return 'chocolate'
groceryListArray[2] //will return 'rainbows'
groceryListArray[3] //will return 'cookies'

// Note that arrays always start at 0!
// Arrays are always encapsulated by square brackets
```

so following our previous haystack example I'm pretty sure you can figure out how arrays and loops interact!

### Your objective for this section:
- [ ] [Go through 'For Loops' section](https://www.codecademy.com/courses/javascript-beginner-en-NhsaT/0/1?curriculum_id=506324b3a7dffd00020bf661)
- [ ] [Search for your name with your new found knowledge!](https://www.codecademy.com/courses/javascript-beginner-en-XEDZA/0/2?curriculum_id=506324b3a7dffd00020bf661)
- [ ] [Go through 'While Loops'](https://www.codecademy.com/courses/javascript-beginner-en-ASGIv/0/1?curriculum_id=506324b3a7dffd00020bf661)
- [ ] [Let's build a Dragon slayer game with your new found knowledge](https://www.codecademy.com/courses/javascript-beginner-en-mrTNH-6VIZ9/0/1?curriculum_id=506324b3a7dffd00020bf661)
- [ ] [Know the available Arrays methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

#### Test:

'Adapted from Code Wars - 8kyu stage written by richardhsu':
##### Write a method smash that takes the given array of words and smashes them together into a sentence and returns the sentence. You can ignore any need to sanitize words or add punctuation, but you should add spaces between each word. Be careful, there shouldn't be a space at the beginning or the end of the sentence!

``` javascript
var words = ['hello', 'world', 'this', 'is', 'great'];

function smash (words) {
// your test, finish this function so that it will return the expected sentence
}

smash(words); // it should return "hello world this is great"
console.log(smash(words)); // If you are using the console on your Sublime editor build system to show your output.
```

Using your editor make sure you have saved your work (smash.js), changed the bottom right setting to javascript for correct syntax highlighting, and pointed the editor at Node. Hit command-B to build (show your console log):

*Make sure you have followed the instructions to setting up your source code editor with Node [here](source-code-editor.md)

![screenshot](/images/smash.png)

Using your previous knowledge of git, cd into the file using your terminal and git add, git commit, and git push it to your github account!


#### If you would like extra practice or extra reading:
- [ ] [Mozilla 'For Loops' Docs](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/for)
- [ ] [Mozilla 'While Loops' docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)

#### Hint for test (while not the cleanest, its one of simpler the ways!):   

``` javascript
var words = ['hello', 'world', 'this', 'is', 'great'];

function smash (words) {
    var sentence = "";
    for (var wordsIndex = 0 ; wordsIndex < words.length; wordsIndex++) {
      if (wordsIndex > 0){   //Think about why this is at the start
        sentence += ' ';  
      }
      sentence += words[wordsIndex];
   }
   return sentence;
};

console.log(smash(words));
```

#### But If you read the Arrays methods you'll realize that you can solve it this way:

```javascript
var words = ['hello', 'world', 'this', 'is', 'great'];

function smash (words) {
  return words.join(" ");
};

console.log(smash(words));
```
