# Installation & Configuration: Source Code Editor + Node + NPM

##### What is a source code editor?

So far you have been doing the coding exercises on your terminal, Chrome Console, and on Code Academy. It's time to get you a proper source code editor. Source code editors are just text editors with the added features for programmers to write and edit source code. Amongst other things it allows for syntax highlighting, autocompletion, bracket matching (which is more important than you'd think). Some also do the compilation, interpretation, and debugging of source code. Some programmers prefer IDEs (Integrated Development Environement) which have source code editors inbuilt amongst other fancy features, but let's get the basics first.

##### Let's get the basics: Sublime Text 3

Sublime text is almost like the rite of passage for most programmers - it is simple to use, with great basic features. It is free to use, albeit with license pop up from time to time, if you pay for it the pop ups go away but it really isn't much of a nuisance.

- [ ] [Download it here](http://www.sublimetext.com/) you can also view the different features it has.

- [ ] [Here is a list of nifty shortcuts and personalization you can do with Sublime Text too](https://scotch.io/bar-talk/best-of-sublime-text-3-features-plugins-and-settings).

##### Let's configure your machine to build Javascript code with NodeJS. We will delve further into Node in the next few modules.

Because most of this course focuses on javascript, it would be good for the editor and your machine to be able to build Javascript. Sadly, NodeJS isn't inbuilt but we'll right this wrong now! Without going into too much details - because there is a module on NodeJS - NodeJS takes Javascript, which traditionally runs only on the browser, and creates an environment that allows you to run it on your machine (or server side).

- [ ] First let's install NodeJS and npm (Scroll down for Windows users)

---

### Mac users:

##### 0. Do you have Xcode command line tools yet? You should have after the Git exercises >:(

```bashrc
xcode-select –install
```


##### 1. Get Homebrew
```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Homebrew is the package manager that the Mac wish it had. You can download most software off Homebrew, if its not on Homebrew, it will most likely be available on Homebrew Cask. If it is not on either, maybe it isn't worth it (just kidding). The terminal will explain what you need to do. If you run into any troubles - Google is your best friend! Try googling the terminal error message. If all else fails - Shoot the mentors an email.

```bash
brew doctor
```


##### 2. Let's get NodeJS & npm

Always run brew update and brew doctor before you download anything off Homebrew. We want to make sure that Homebrew is working fine and that everything is up to date.
```bash
brew update
brew doctor
```
```bash
brew install node
```

npm (node package manager comes with node)

---

### Windows users:

##### 1. [Download the NodeJS .msi package](https://nodejs.org/en/download/)

##### 2. Run the .msi file installer and follow the steps


---

### For all users


##### 1. To see if NodeJS is properly installed, go to your terminal

```bash
node -v
```
It should print the version number.

##### 2. Similarly, to see if npm is properly installed, type

```bash
npm -v
```
You should also see the version number

##### 3. To see it in action let's create a hello.js file on Sublime Text

In your Sublime Text create a file called 'hello.js' .js extension declares that it is a javascript file. Inside the file type:

```javascript
#hello.js

console.log('Hello world, I am running this with NodeJS!');
```
Save the file and remember where you saved it to! (For convenience let's save it on your Desktop). Go to the path where you saved hello.js, which in this example is on your Desktop

```bash
$ cd ~/Desktop
$ node hello.js
```
You should see the message logged right back at you! :)

##### 4. Set up Build System on Sublime Text

Alright, we've set up NodeJS and npm on your system, let's set it up on the Sublime Text build system.
- On the top navigation bar, go to "Tools > Build System > New Build System"
- In the new build page insert this:
```yaml
{
"cmd": ["node", "$file"],
"selector": "source.js"
}
```
If you run into a "[Errno 2]" error, then you'll need to change "node" in the code above to the path where node is located. To do this, open terminal and run "which node". This will print out the path to the node binary. For example:
```yaml
{
  "cmd": ["/usr/local/bin/node", "$file"],
  "selector": "source.js"
}
```
- Save the file as "node.sublime-build" in the default "user" folder.


##### 5. How to use the Build System on Sublime Text

- Open up the hello.js you created for the previous steps in sublime text, it should console.log something.
- Go to "Tools > Build System" in the top bar and select "node".
- Build the Javascript file, using either the build shortcut (Ctrl+B for Windows, and ⌘ Command+B for Mac), or by choosing "Build" from the "Tools" menu.

###### Ta-da your code should be build right infront of you!
