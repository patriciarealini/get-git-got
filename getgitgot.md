#GET GIT GOT
*An Introduction to the Command Line, Git & GitHub*

####What You Need
* Install [Git](http://git-scm.com/download)
* Create a [GitHub Account](https://github.com/)

##What is the Command Line?

Do you recall the days of DOS? When you turned on the desktop and the screen was not a high resolution lavender nebula but just black & the text was "ugh i've been slimed!" green? That was the terminal. It's still there, hiding behind your flip clock screensaver & your desktop widgets. 

["The command line is an interface that allows you to talk directly to your computer using words called commands."](http://www.freesoftwaremagazine.com/articles/command_line_intro) 

Commands are formatted without spaces. i.e. `command` Some commands can be modified. Modifications are made through options, commands that come after the command. Options are preceded by a dash. i.e. `command -option`

Option `--help` will spell out the details of the command you precede it with.

* Windows --> cmd.exe
* Mac --> Terminal

Quick Tip: A directory is just another name for a folder.

##Basic Commands for the Command Line

| Command 			|	Use 										|
|-------------------|-----------------------------------------------|
| `whatis`			|	a look up command i.e. `whatis cd`			|
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

##Git

Distributed Version Control System - DVCS makes it possible to track the changes various authors make to a file or set of files & smoothes out the process of combining their files while preserving old versions. Makes for easier collaboration & effective combining of changes. If you want to learn more about Version Control i recommend this [Git Tower](http://www.git-tower.com/learn/cheat-sheets/vcs-workflow) guide. 

Just like with the Command Line, commands are formatted without spaces and can be followed by an option. However, all Git commands begin with the word `git`. 

Why learn Git? With applications like the GitHub software, there doesn't seem to be a use for using the terminal, except the software can be problematic. Learning the basics of git is honestly faster, just as easy & prepares you to better understand what you're doing. 

##GitHub

The platform. A web based repo hosting service. 

Repository - a directory that is enabled to interact with Git & GitHub. Abbreviation: repo. 

Within each repo there are three trees...

1. Working Directory - houses the files (what you see in your folder)
2. Index - the staging area
3. HEAD - the last commit

Commit - a snapshot of the file at a specific state. 

Branch - a separate work area. A version of the repository that authors can change without affecting the master branch but can later merge with the master branch to make a big change all at once. 

Staged - files ready to be committed.

Unstaged - files that have been changed and not ready to commit

Untracked - files that git doesn't track, usually new.

Deleted - a file you have removed from a folder but is waiting to be removed from the repo via git.

Origin - references the working directory you are interacting with

Push - The final command to commit changes made in the working directory to the branch

Pull - a command used to update your working directory with the latest changes to the branch.

##Setting up your Terminal with GitHub

Log into GitHub via your terminal (you will only have to do this once)

1. `git config --global user.name "John Doe"`
2. `git config --global user.email johndoe@gmail.com`

##Repositories

To set up your repo with the terminal, first you must turn a directory into a repo with `git init`. Then go to [GitHub New Repo](github.com/new) or click on the + in the upper right hand corner of github in the browser & select new repository. Match the name of your GitHub repo with the name you gave the directory/repo on your computer. Go back to the Terminal & enter `git remote add origin url.git`. Then enter `git push -u origin master`.

##Commit & Push

Now that we have a repo to work in we can start adding files & working on them. Remember, the whole reason for working with GitHub is to have a record of changes you make to your file, so start committing right away! To demonstrate we will start by creating a README file. Create the files & place it in the working directory for your repo. (If you're a command line wiz you can do this without leaving your terminal, a challenge for those that want to learn more. Check out the Art of the Command Line for more info.)

1. Check your repo for unstaged/staged/tracked/untracked files by entering `git status` in the terminal. You should see `README.md` in red under "Changes not staged for commit".
2. To move the README into the staging area. Enter `git add README.md`. 
3. Enter `git status`. This time, README should be in green under "Changes to be committed".
4. Enter `git commit -m "adding README file"`. the `-m` stands for message. The string in parenthesis will be tied to the changes you made in this commit so that you and other users can look back with ease & not have to read all the code. Commits will be rejected without a message. 
5. Enter `git status`. There should be no trace of your README file. README has been committed to your repo & now we need to push it to the branch. (We'll get to branches in a minute.)
6. The last step to finalize the update is pushing the changes to a repo & branch on github. For this step we will enter `git push origin master`.

You did it! You just made your first commit & your first push!

##Branches

Branches are places where you can make changes, without affecting the master branch. It's important to start working this way from the get-go because when you get on bigger & bigger projects, you will want to test your changes before you make them public. You can have as many branches as you want. Let's make our first branch!

1. Enter `git branch` to check the branches available to you at this time. Your terminal should output `* master` since you haven't yet made any other branches.
2. Enter `git branch testingbranch` to create a new branch called testingbranch. 
3. Enter `git branch` to verify the creation of testing branch. This time your Terminal will output `* master    testingbranch`
4. Enter `git checkout testingbranch` to switch over to the testingbranch. Now all the commits you make need to be pushed to the branch you are in. From now until you switch, pushing will be finalized with the command `git push origin testingbranch`.

Quick Tip: You can bypass step 2 by modifying step 3 to `git checkout -b testingbranch`. This does step 2 & 3 at the same time. 

Quick Tip: Once you've settled into a branch & will only be pushing to that one branch, you can command the push with `git push -u origin testingbranch` and shorten your push command to `git push` until you change branches. You will have to switch it in your push command by reverting back to the older command `git push origin branchname`. 
 

##Tracking Changes

##Cloning
`git clone url`

##Pull

##Merge

##Conflicts

##Forking

##Resources

###Walkthroughs
* [Try Git](https://try.github.io/)
* [Git Immersion](http://gitimmersion.com/)
* [Roger Dudler's Git Guide](http://rogerdudler.github.io/git-guide/)
* [Think Like a Git](http://think-like-a-git.net/)
* [A Visual Git Guide](http://marklodato.github.io/visual-git-guide/index-en.html)
* [Git Tower](http://www.git-tower.com/learn/)
* [Git & The Terminal](https://18f.gsa.gov/2015/03/03/how-to-use-github-and-the-terminal-a-guide/)

###Self Directed
* [Pro Git](http://git-scm.com/book/en/v2)
* [First Aid Git](http://firstaidgit.io/#/)
* [Understanding GitHub](http://readwrite.com/2013/09/30/understanding-github-a-journey-for-beginners-part-1#awesm=~oGqRd1nOhtuidI%3F_escaped_fragment_=)
* [Git Youtube Videos](https://www.youtube.com/playlist?list=PLg7s6cbtAD165JTRsXh8ofwRw0PqUnkVH)
* [Git Dev Docs](http://devdocs.io/git/git)
* [Git Cheat Sheet](http://overapi.com/git/)
