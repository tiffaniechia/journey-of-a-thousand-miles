## Git

Git is one of the most widely used version control system for all things code. So what is version control?

Most code bases are fairly large and worked on across multiple individuals. Changes and additions to the code base is then being tagged by what we call 'commits' so that the broader population looking at the code base know why a certain chunk of code was added or removed. The other handy thing about version control, as the name suggest, is to have more control over the versions - the ability to roll back or cherry pick commits to your code base. Think about it like saving and undo-ing a document - you want to have the ability go back in history and undo any of your changes, and saving your work as you go along. It's like writing a thesis without the 'save' and 'undo' functions, you won't write thousands of words without pushing the save or undo buttons, would you?

There are other control systems out there - Subversion is a predecessor of Git, still used in many enterprises, however it is a lot less verbose than Git. Someone once described it in terms of packing for traveling - Subversion is like immediately dumping everything you see into your suitcase and then zipping it up. Git is like putting everything on your bed first,  then making sure you really need the clothes first before putting them into your suitcase. The success of Git over Subversion can be sneakily seen by the creation of 'git svn'. Git-SVN was made for people who for whatever reason, had no choice but to use Subversion. Git svn provided a backdoor into Git allowing developers to use Git locally.

And thank goodness you completed the first section of this course about the command line! Git is controlled using the command line interface - there is no save or undo button for your wider code base!


#### GitHub

GitHub is a Git repository hosting service- at the very basic, think about it like the dropbox for code with a great user interface. Amongst other things it is a platform for open collaboration - open source is how some of the greatest software were and are being made. GitHub also allows you to follow users whose repositories you admire!

GitHub's mascot is an animal known as an Octocat, half octopus, half cat, and there lives  an Octocat skeleton sitting in a glass case inside the GitHub office. Just imagine the faces of the archeologists who dig it up 10000 years from now.


#### Your objective for this section:

- [ ] Go through the exercises on [Try Git](https://try.github.io/levels/1/challenges/1). Make time to go through the 'repository' and understand the console output and what which command does.
- [ ] * Git will not be preinstalled in your systems, to complete the exercises you will need to [follow the instructions here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
- [ ] When you're feeling more comfortable with Git, let's delve deeper into it with [Git Immersion](http://gitimmersion.com/). This uses a bit of Ruby - but nothing too complex.
- [ ] [Create a GitHub account](https://github.com/).
- [ ] Complete Test:
  - [ ] Create your first repository ('my-first-repository')
  - [ ] With your new found command line skills, create a file on your desktop, within this file, create a README.md file (markdown file), initialize it, add remote origin pointing to your first GitHub repository, write into your README.md ('hello world!') using your command line, git add your file, git commit your file with the message (my first git commit message!), and push it to GitHub.

#### Hint for test:  
```bash
$ cd ~/Desktop
$ mkdir my-first-repository && cd my-first-repository
$ git init
$ git remote add origin git@github.com:YOUR_GITHUB_USERNAME/my-first-repository.git
$ touch README.md
$ echo ' hello world' > README.md
# or if you did the vim tutorial, try writing into it with vi :)
$ git status # it is red because it's untracked
$ git add README.md
$ git status # it is green now because you added it!  
$ git commit -m "my first commit message"
$ git log # check out your commit message!
$ git push origin master
# now go to your GitHub repository and see it! :D
```
