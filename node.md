##Node.js

###BE vs FE


When beginning web development, you will hear about people working in the back-end, front-end or being full stack developers. So what does that mean? What do they do?

A *front end developer* will worry about things like how your site looks, and will work on what you see and how you interact with the site (e.g. what happens when you tick a box or click a button, or select a menu item from a list).

The general knowledge of a FE dev would be: 

- HTML, CSS, SASS, LESS (and CSS frameworks, such as [Bootstrap](http://getbootstrap.com/), [Materialize](http://materializecss.com/), etc.)
- Javascript, jQuery, AJAX
- one or more of the many Javascript-based frameworks ([Angular](https://angularjs.org/), [ReactJS](https://facebook.github.io/react/), Backbone,js, Ember, etc.)

A *back end developer* is someone who does all the logic behind the site, and that provides the front end developer with the information needed for actually rendering(or creating the visual of) the site.
Things like storing your address on a shopping site, so that if you log in after 2 months you don't have to re-add it; or storing the read/unread messages from your inbox so that you can access them from anywhere; are things that the BE devs care about.

Technologies for a BE dev include:

- languages: Ruby, Java, Python, Javascript etc.
- runtimes & frameworks: Node.js(javascript), Express(javascript), Ruby on Rails(Ruby), Sinatra(Ruby), Django(Python), and others.

A *full stack developer* is simply a developer that is able to do both front and back-end work at reasonably good level, meaning that she or he is specialized both in front end as well as in back end.

####How do the BE and the FE communicate with each other?
Let's take a concrete example:

Let's say I have a grocery list that I am trying to see on my site from any device(my mobile, my mom's computer, etc), at any time(now or in a week).

Given that I want to see my list anytime/anywhere, the BE developer will save this list in a database (or persistently store).
Because I want to see my grocery list, she/he will retrieve it and make it available in a place called and API endpoint. The information placed here is normally in a JSON format and looks something like:
```
{
	'croissant': 2,
	'milk': 1,
	'eggs': 3,
}
```
This is where the FE developer comes in.
She/He takes this info from the endpoint by doing a GET request, and will for instance show it in a list where I can tick what items I've bought, or let me change the quantity of the products, or add more products to my list or delete products and so on.

If let's say I've forgotten to add 2 oranges, and I want my list to be permanently updated with the addition of these oranges; I, as a user will add the oranges to the list - letting me add another product is something the FE dev does, and the FE will now make sure the BE knows you also want oranges, by sending a POST request to and endpoint where the BE is listening. The BE sees the update and makes the change in the database, so that the next time you want to see your grocery list, it will now know you also have oranges in the list.

You can read more about GET, POST and other request types [here](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods).

###What is Node?
Node is a runtime build using javascript. It is event-driven, non-blocking and lightweight.
It is used in the Back End, and with it you will normally create your own server.

You will often hear about Node and Express together, and for now it is good to know that Express is just a framework build on top of Node. We will talk more about express in the following lessons. [See differences between a framework and a runtime enviroment here.](http://stackoverflow.com/questions/5372852/meaning-of-runtime-environment-and-of-software-framework)

- light weight - Node is very bare bones, most of what you need you will have to import gradually, using npm(node package manager) packages. Fortunatelly, there are zounds of npm packages available that do just about everything you want: from helping you format time to talking to the TwitterAPI.

- non-blocking - if you trigger an event e.g. you make a request to an external resource, between the time you've started this request and the time you get the response from this request, you can still interact with your program. In contrast, a blocking application would not let you execute any action during this time.
The non-blocking events are called asynchronous or async events, while the blocking event are sync or synchronous events.

An excellent video on the event loop, sync and async actions can be found [here](https://www.youtube.com/watch?v=8aGhZQkoFbQ).

###Getting Started
There are more way of installing node on your computer, this is one that I personally like.

On your terminal window:

1. If you do not have it yet, first install [homebrew](http://brew.sh/), instructions are on the site, please find them below as well:
  - `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
  - `brew install wget`

2. install node:
  - `export PATH="/usr/local/bin:$PATH"`
  - `brew install node`

 3. see what version of node you have and try running node:

	- `node -v`
  - `node`

The last command should let you write javascript commands on your terminal.
If you want to exit just press `ctrl+c` twice.

You should be ready to go!

A good tutorial available for free is from [nodeschool](http://nodeschool.io/), and I think that is a good starting point.

To run the tutorial, go to your terminal/console and run:
- `npm install -g learnyounode`
- `learnyounode`

Nodeschool also organizes a nodeschool day where you can go and run through the tutorials for an entire day, with volunteer assistants that can help you if you get stuck.
Definitely recommended.


###Links
* [Differences between a framework and a runtime enviroment](http://stackoverflow.com/questions/5372852/meaning-of-runtime-environment-and-of-software-framework)
* [NPM resources](npmjs.com)
* [Sync/Async actions and the event loop](https://www.youtube.com/watch?v=8aGhZQkoFbQ)
* [Nodeschool - node tutorial](http://nodeschool.io/#workshoppers)
