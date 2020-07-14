# Git

### Hi everyone. My name Is Mohammad Samara, and I will share with you what I have learned about **Git**

Git is a DVCS (Distributed Version Control system) that stores data in a file system made up of snapshots, it works locally on your pc to keep tracking your code and files changes. Also it will allow you to view,apply,and remove these changes.

    * Version Control is a system that allows you to see all the versions of a file by recording changes. with it you can go back to a previous version of the file, track modifications , and compare changes. By using a Version Control System (VCS), mistakes with files can be reduced significintly.

## how it works?
* Each time you save a changed version of your project (called commit) Git creates a snapshot of the file at points of time, and it keeps a history of what these snapshots look like.
* Also it has a special label called **Head** which tell as that we are here (at a specific version of the file)
* git keep tracking all the changes of the file at different point of time.
* you usually give a snapshot a label called message describing why you did the changes.

## how to use it?
After installing Git on your computer you can access it's commands through *Ubuntu*

##### Cloning

You can create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:
$ git clone (https://github.com/"repository’s name")

##### Check File Status
use the command ($ git status)

##### Tracking and Staging a New File

   * Single File

Track one file only by using the following format:

git add filename

   * All Files

Track all files in a repository by using the following command:

$ git add *

*After using these commands, files are tracked and staged for committing.

##### Committing a File

After staging one or multiple files, you should commit the changes and record what you did within the commit message:

$ git commit -m “made change x,y,z”

##### Pushing Changes

Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.

Example:

$ git push origin master

# what is **GitHub** ?

it's an online place to store your code and share it with others, and it uses Git to make collaboration possible by:

* version tracking
* reviewing changes
* keep changes separate untill you want to add them

#### **with Git and GitHub together you can work and edit codes offline and publish it on the cloud when you want.
