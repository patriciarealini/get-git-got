#GET GIT GOT

####What You Need
* Install [Git](http://git-scm.com/download)
* Create a [GitHub Account](https://github.com/)

##What is the Terminal?

Do you recall the days of DOS? When you turned on the desktop and the screen was not a high resolution lavender nebula but just black & the text was "ugh i've been slimed!" green? That was the terminal. It's still there, hiding behind your flip clock screensaver & your desktop widgets. 

* Windows --> cmd.exe
* Mac --> Terminal

Directory === Folder

##Basic Commands for the Command Line

| Command 			|	Use 										|
|-------------------|-----------------------------------------------|
| `cd`				|	change directory 							|
| `cd ..` 			| 	go back one directory 						|
| `cd - `			| 	go back to previous working directory 		|
| `ls`				|	list (files in directory) 					|
| Tab				|	completing arguments 						|
| CTRL-P/CMMD-P		|	recalls the previous command  (up arrow) 	|
| CTRL-R/CMMD-R 	|	search command history 						|
| CTRL-W/CMMD-W 	|	deletes the last word						|
| CTRL-U/CMMD-U 	|	deletes the whole line 						|
| CTRL-L/CMMD-L		|	clear screen 								|

For more info, check out [The Art of the Command Line](https://github.com/jlevy/the-art-of-command-line)

##What is Git?
Distributed Version Control System - it tracks the changes, preserving old versions & changes made. Makes for easier collaboration & effective combining of changes 

>"Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later."

##What is GitHub?
Allows you to make changes to your version without affecting the shared project. 
Changes you make can be cleanly housed within your branch and then merged to the master branch when ready

##Setting up your Terminal
Log into GitHub via your terminal

1. `git config --global user.name "John Doe"`
2. `git config --global user.email johndoe@example.com`
3. z

##Interacting with GitHub one-on-one

###Commit & Push
`git status`
`git add filename.py`
`git status`
`git commit -m "adding filename"`
`git status`
`git push origin branchname`

###Branches

###Tracking Changes

##Interacting with GitHub as a team

###Cloning

###Pull

###Merge

###Conflicts

##Interacting with other people's GitHub

###Forking

##Resources
Pro Git
[First Aid Git](http://firstaidgit.io/#/)
[Understanding GitHub](http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1#awesm=~oGqRd1nOhtuidI%3F_escaped_fragment_=)
[Git Youtube Videos](https://www.youtube.com/playlist?list=PLg7s6cbtAD165JTRsXh8ofwRw0PqUnkVH)
