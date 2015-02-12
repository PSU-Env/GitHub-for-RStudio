# GitHub-for-RStudio

This page is a reference for setting up GitHub for a group to work with R projects in RStudio. The three steps outlined below are designed to setup a fork from a main project directory in GitHub so that multiple people can collaborate on a project. The assumption is that you have already setup a [GitHub](https://github.com/) account, and installed both [R](http://www.r-project.org/) and [RStudio](http://www.rstudio.com/) on your machine.  

If you do not have push access to the main repository, at the bottom are [directions](https://help.github.com/articles/merging-an-upstream-repository-into-your-fork/) for keeping your repository up-to-date with the upstream repository.  

--------
**1 Download Git for your operating system ([link](http://www.git-scm.com/downloads)):**  This program allows R to interface with GitHub. **After installing Git:** *In RStudio select Tools, then Global options, then Git/SVN.  Enable version control for RStudio, then browse to your directory that has **git.exe.** Select OK, then restart R.*  

![](gitSetup.png)

**2 After you open a GitHub account, navigate to the repository that is setup for your group, click on the "Fork" icon at the top of GitHub page.**  This creates a copy (clone) of the master project directory that is now your repository **(repository = Project in R).**  *Copy the HTTPS clone URL from the box next to your repository on the right. Check the link, it should have your GitHub user name in it.*

![](fork.png)
![](clone.png)

**3 In RStudio, select new project, then version control, then Git.**  Here is where you will paste the link from the GitHub clone (step 2 above). *Click Tab key and R will create a project name from the one used in GitHub.*

![](proj.png)

**Finishing step 3 will automaticly copy all files into your new R directory on your PC.**  These are all the files currently in the main GitHub directory that you forked, so you dont have to start from scratch.  

More detailed description for setting up Github with RStudio from Ecologist ([link](http://www.molecularecologist.com/2013/11/using-github-with-r-and-rstudio/)), and 
Rstudio ([link](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN)).

--------
**Update your Forked directory with your groups upstream Main Project** ([link](https://help.github.com/articles/merging-an-upstream-repository-into-your-fork/)). Or, ([link](https://help.github.com/articles/syncing-a-fork/))

As contributions are submited to the main project repository with a pull request from folks in your group, you might want to update your directory to include the new changes.

In GitHub, copy the link from the main project directory. *Do not copy the link from your forked directory*.  In RStudio, select Tools, then Shell. At the Shell command prompt type:

`> git pull https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git BRANCH_NAME`  

If there are no conflicts, this will update all files in your main PC directory with the main project on GitHub.  You can now push these changes to our Forked GitHub Repo using the Push option in RStudio.

Here is the [link](http://psu-envstats.github.io/GitHub-for-RStudio) to a web site with the same information.  

--------
**For Mac IO**

After installing Git, on your computer, open the Terminal application.
 
Tell Git your name so your commits will be properly labeled, this should be the same as your user name in GitHub. Type everything after the $ here:
`$ git config --global user.name "YOUR NAME"`
 
Tell Git the email address that will be associated with your Git commits. The email you specify should be the same one found in your email settings in GitHub.
`$ git config --global user.email "YOUR EMAIL ADDRESS"`



