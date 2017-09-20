DRAFT DOCUMENT
## Minimal Command Line git
### Introduction
This documnet attempts to layout a work flow for using GitHub and Git as our version control software in this course covering HTML, CSS
and a tad of JavaScript. The original hope was that, since our results were all plain text, that we could build and maintain our work in
GitHub alone, but issues such as privacy kept raising their heads causing roadblocks in such an approach, so I surrendered and 
decided to bite the bullet and introduce as little command line Git as we could get by with. Along those lines 
[Useful Reference](https://github.com/GarageGames/Torque2D/wiki/Cloning-the-repo-and-working-with-Git), I think, is a very good reference for that level and may even touch slightly on topics that we do not need here. If you view this page be sure to checkout the 
three links in the recommendations section at the bottom of the page. They may be more helpful than this initial page itself.  
As I have mentioned our requirements are minimal as far as GitHub and Git go, so I have listed in the following section the assumptions upon which the workability of the work is predicated.  
## Assumptions

1. The reader has a GitHub account and access to a private repository already defined in GitHub where the work will be kept. 
1. That repository always contains the latest frozen version of the application in the **master** branch, and
1. that a development branch has been created which I will refer to as **work**.
1. The reader is prevented from merging into the **master** branch without an approved review from an administrator of the repository.  

Briefly speaking, the work flow will go as follows:
1. The repository will copied (cloned) to a directory on a local machine.
1. There the application will be built, modified or enhanced using tools on the local machine, such as Notepad++, NetBeans, Android Studio.
1. After testing, the version of the application in the GitHub repository will be updated with with the modification, and
1. A Pull Request comparing the **master** and **work** branches will be created.
1. Following the review of the PR, the reader will either make requested changes or correction and resubmit the PR or, upon an 
accepted review, will merge the **work** branch into the **master** branch and delete the **work** branch.

### Work Flow

1. **git config --global user.name "David Murrell"**

   Tell git your name so it can use in any commits you might use. 
   **
1. **git config --global user.email "dmurrell@faulkner.edu"**

   Similarly, tell git your name for it to include in any commits. 
   
1. **git clone https://github.com/FU-CIS3360-FALL2017/javajam-coffee-house-bp90347.git**  

   Download a copy of a repository from GitHub to your local machine.
   
1. **git checkout chapter4**  
1. Change or add files using local machine tools
1. Test application using local machine tools
1. **git add ***  
1. **git commit -m 'commit title'**  
1. **git push origin chapter4**
1. Inspect changes in GitHub
1. Create a Pull Request in GitHub
1. Respond to PR review

### Comfort Commands

1. **git remote -v**
1. **git branch -v** 
1. **git status**
1. **git log**
1. **git diff master chapter3**
1. **git pull**
