## Command Line

While the direct benefits of mastering the command line is not immediately obvious, it is definitely a key skill every developer should have under their belt.

You don't need to know all the commands from the command line interface, but there are some key commands that you will use often enough and some that will make life a lot easier for your life as a developer.

The command line is at its very basic, the computer as you know it. All the icons you see are Graphical User Interfaces (GUI) made for the wider public who are not command-line savvy. The GUI is far behind the command line in terms of functionality - as you move forward you will find that it will be much quicker, and some times, only possible to do things via the command line. You can even send emails and order Dominos via the command line! Almost anything you can do with your mouse and GUI, you can do via the command line :)  

The command line is the entry point to all the inner workings of your computer, which brings me to the topic of scripts. As you advance you will want to automate some tasks, this is where scripts come in. The best developers are the laziest people, not because they don't do anything but because you create scripts to automatically run things they are too lazy to do. Assuming you are using a Unix based systems - a well written bash script can do anything - only limited to your imagination and skills to execute said imagination. A good grasp of the command line can allow you to write some very amazing scripts.

#### Your objective for this section:

- [ ]  Complete ['Learn enough command line to be dangerous'](http://www.learnenough.com/command-line-tutorial) by Michael Hartl. Do Work through all the exercises. If you are using a MacBook, you can skip Box 2 in section 1 of the tutorial.


#### Test:  
  - [ ] Know the difference between ~ and / (Google it :D)
  - [ ] Understand the importance/danger of sudo.
  - [ ] Using only your command line: Create a txt file named 'hello.txt' on /tmp, write into it 'omg I am writing into the file via the command line!', close it then cat the file, create a directory on your user home desktop path named 'foo', move hello.txt into ~/Desktop/foo, rename hello.txt to helloagain.txt, and chmod removing all write permissions to the file (you will find yourself unable to write into it now, now you just created permissions controls for your file!).

#### If you would like extra practice:

- [ ] [Code Academy Command Line Course (estimated 3 hours)](https://www.codecademy.com/learn/learn-the-command-line)

#### God-mode brownie points:
- [ ] [Learn the basics of Vim](http://www.openvim.com/) The reason why I am an advocate for vim is the effortless ability to view and edit files on the command line which is an important skill to have as you move on.

#### Hint for test:  
```bash
$ cd /tmp
$ touch hello.txt
$ echo 'omg I am writing into the file via the command line' > hello.txt
$ cat hello.txt
$ cd ~/Desktop
$ mkdir foo
$ mv /tmp/hello.txt ~/Desktop/foo
$ mv ~/Desktop/foo/hello.txt ~/Desktop/foo/helloagain.txt
$ chmod -w ~/Desktop/foo/helloagain.txt
# try writing into it
$ echo 'this will throw an error' > ~/Desktop/foo/helloagain.txt
permission denied: helloagain.txt
 ```
