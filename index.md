In the repository [scripts]https://github.com/FU-CIS3360-FALL2017/scripts.git) of this same organization there are two scripts designed to relieve the user of
remembering a good bit of keyboard detail that is required in the work flow of this document. These scripts essentailly 
automate the work flow herein in two parts.
## Minimal Command Line git
### Introduction
This documnet attempts to layout a work flow for using GitHub and Git as our version control tool in this course which covers HTML, CSS
and a tad of JavaScript. The original hope was that, since our results were all plain text, we could build and maintain our work in
GitHub alone, but issues such as privacy kept raising their heads causing roadblocks in such an approach, so I surrendered and 
decided to bite the bullet and introduce as little command line Git as we could get by with. Along those lines 
[Useful Reference](https://github.com/GarageGames/Torque2D/wiki/Cloning-the-repo-and-working-with-Git), I think, is a very good reference for that level command line Git and may even touch slightly on topics that we do not need here. If you view this page be sure to checkout the three links in the recommended readings section at the bottom of the page. They may be more helpful than the initial page itself.  

As I have mentioned our requirements are minimal as far as GitHub and Git go, so I have listed in the following section the assumptions upon which the workability of the subsequent work flow is predicated.  
## Assumptions

1. The reader has a GitHub account and access to a private repository already defined in GitHub where the application is to be maintained. 
1. That repository always contains the latest frozen version of the application in the **master** branch, and
1. That a development branch has been created which I will refer to as **work**.
1. The reader is prevented from merging the **work** branch into the **master** branch without an approved review from an administrator of the repository.  

Briefly speaking, the work flow will go as follows:
1. The repository will be copied (cloned) to a directory (folder) on a local machine.
1. There the application will be built, modified or enhanced using tools on the local machine, such as Notepad++, NetBeans, Android Studio, browser of your choice.
1. After testingon the local machine, the version of the application in the GitHub repository will be updated with the modificationd from the local machine, and
1. A Pull Request comparing the **master** and **work** branches will be created.
1. Following the review of the PR, the reader will either make requested changes or correction and resubmit the PR or, upon an 
accepted review, will merge the **work** branch into the **master** branch and delete the **work** branch.

### Work Flow
1. On your local machine, create a folder named, perhaps, **MyRepos**, right-click that folder and select **Git Bash Here**.
   You should find yourself in a command line environment that is actually simulating a Unix/Linus command line. In this environment 
   you will be able to issue **git** commands. You must, however, type the word **git** before each command as indicated in the 
   work flow commands following. You can also use Unix commands such as *ls* in this command line. Type *exit* to close the command line dialog.

1. **git config --global user.name "David Murrell"**

   Tell git your name so it can use it in any commits you might use. 
   
1. **git config --global user.email "dmurrell@faulkner.edu"**

   Similarly, tell git your name for it to include in any commits or to send you email. 
   
1. **git clone https://github.com/FU-CIS3360-FALL2017/javajam-coffee-house-bp90347.git**  

   Download a copy of a repository from GitHub to your local machine. The files of the downloaded repository will appear in a
   directory (folder), referred to as the **working directory**, in the **MyRepos** folder. This folder will have the name of the downloaded repository. 
   
1. **git checkout work**  
   
   Ask git to provide the files of the **work** branch in the working directory.
   
1. Change or add files using local machine tools
1. Test application using local machine tools
1. **git add \***  

   Ask git to add all files in the working directory that have been added or changed to the git **staging** area.
   
1. **git commit -m 'commit title'**  

   Ask git to take a snapshot of the files in the **staging** area and place it in the **head** area. These are the files and commit history that will
   be sychronized with the **work** branch on GitHub when the **push** command is next given.
   
1. **git push origin work**

   Ask git to synchronize the files in the **head** area with the **work** branch on GitHub. Remember that *origin* is what
   Git calls the URL of the GibHub repository from which it cloned the local repository.
   
1. Inspect changes in GitHub.
1. Create a Pull Request in GitHub.
1. Respond to PR review.

### Comfort Commands

1. **git remote -v**

   List the names of the remote (web) repositories that are known to this git session. Git can use two different GitHub repositories
   from which it downloads (fetches) information and to which it will upload (push) information, but in our case these will be the
   same and you will see that in the listing produced by this command. The letter v in the option -v stands for *verbose* and its
   usage will get you a more complete (wordy) listing than without it.

1. **git branch -v** 

   List the branches that are present in the downloaded repository. The one preceded by the asterisk is the branch currently
   in the **working directory**.
   
1. **git status**

   Display paths that have differences between the **staging** area and the current **head** commit, paths that have differences
   between the **working directory** and the **staging** area, and paths in the **working directory** that are not tracked by Git.
   
1. **git log**

   Show the commit history.
   
1. **git diff master work**

   Show differences between the **master** branch and the **work** branch. 
   
1. **git pull**

   Incorporates changes from a remote repository into the current branch. If, after cloning a repository, you have made change to
   the remote (GitHub) repository, this command will will bring down those changes and apply them to the current branch in Git.
   
