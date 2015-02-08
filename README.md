# Github-for-R

This site is for setting up GitHub to work with your R projects.

Here is the link:  http://psu-envstats.github.io/Github-for-R. 

--------
- 1 **Download Git for your operating system ([link](http://www.git-scm.com/downloads)):**  This program allows R to interface with Github. **After installing Git:** *In R select Tools, then Global options, then Git/SVN.  Enable version control for RStudio, then browse to your directory that has git.exe. Select OK, then restart R.*  

![](gitSetup.png)

- 2 **After you open a Gitbub account, click on the "Fork" icon at the top of Github page.**  This creates a copy (clone) of the master project directory that is now your repository **(repository = Project in R).**  *Copy the HTTPS clone URL from the box next to your repository on the right. Check the link, it should have your Github user name in it.*

![](fork.png)
![](clone.png)

- 3 **In R, select new project, then version control, then Git.**  Here is where you will paste the link from the Github clone (step 2 above). *Click Tab key and R will create a project name from the one used in Github.*

![](proj.png)

- **Finishing step 3 will automaticly copy all files into your new R directory on your PC.**  These are all the files currently in the main Github directory that you forked, so you dont have to start from scratch.  

More detailed description for setting up Github with R from Ecologist ([link](http://www.molecularecologist.com/2013/11/using-github-with-r-and-rstudio/)), and 
Rstudio ([link](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN)).

--------
**Update your Forked directory with upstream Main Project** ([link](https://help.github.com/articles/merging-an-upstream-repository-into-your-fork/)).

In Github, copy the link from the main project directory ([link](https://github.com/PSU-EnvStats/Ev567Proj)). *Do not copy the link from your forked directory*.  In R, select Tools, then Shell. At the Shell command prompt type:

`> git pull https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git BRANCH_NAME`  

If there are no conflicts, this will update all files in your main PC directory with the main project on Github.  Push these changes to our Forked Github Repo using the R Push option.
