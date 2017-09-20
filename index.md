DRAFT DOCUMENT
## Minimal Command Line git
### Introduction
[Useful Reference](https://github.com/GarageGames/Torque2D/wiki/Cloning-the-repo-and-working-with-Git) 

### Work Flow

1. git config --global user.name "David Murrell" 
1. git config --global user.email "dmurrell@faulkner.edu" 
1. git clone https://github.com/FU-CIS3360-FALL2017/javajam-coffee-house-bp90347.git  
1. git checkout chapter4  
1. **Change or add files using local machine tools**  
1. **Test application using local machine tools**
1. git add *  
1. git commit -m 'commit title'  
1. git push origin chapter4
1. **Inspect changes in GitHub**
1. create a Pull Request in GitHub
1. response to PR review

### Comfort Commands

1. git remote -v 
1. git branch -v 
1. git status
1. git log
1. git diff master chapter3
1. git pull
