***

### I'm getting an error message. What's wrong?

Take a look at our [Common Errors and Fixes](https://github.com/swirldev/swirl/wiki/Common-Errors-and-Fixes) page.

***

### Automatic submission failed. How do I submit manually?

If automatic submission failed, then swirl created a file in your current working directory that can be used for manual upload. You should have seen something like this:

```
| To notify Coursera that you have completed this lesson, please upload
| ‘rprog-003_Basic_Building_Blocks.txt’ to Coursera manually. You may do
| so by visiting the Programming Assignments page on your course website
| and selecting the Submit button next to the appropriate swirl lesson.
| I've placed the file in the following directory:

/Users/nick/Dropbox/R_Working_Directory
```

On the Programming Assignments page, there is one submit button for each part of the assignment:

![Submit button](https://dl.dropboxusercontent.com/u/14555519/Screenshot%202014-04-07%2017.41.13.png)

Click the appropriate Submit button and upload the file that swirl created for you.

***

### Why do I have an old version of swirl even though I followed the instructions for installing the most recent version?

If you followed [these instructions](https://github.com/swirldev/swirl#installing-swirl-from-cran) for installing swirl from CRAN, then one of two things is preventing you from getting the most recent version.

1. You have an old version of R. You must have R version 3.0.2 or later to install the most recent version of swirl. You can check what version of R you have by typing `R.version.string` at the prompt.
2. Your default CRAN repository is out-of-date. You can check what CRAN repo you're using with `getOption("repos")`. We recommend using the RStudio CRAN repository. More info [here](http://blog.rstudio.org/2013/06/10/rstudio-cran-mirror/).

***

### Why am I not seeing the R Programming course in swirl?

If you weren't prompted to install the R Programming course when you started swirl for the first time, then you must have an old version of swirl. See the answer to [this question](https://github.com/swirldev/swirl/wiki/Coursera-FAQ#why-am-i-getting-an-old-version-of-swirl-even-though-i-followed-the-instructions-for-installing-the-most-recent-version).

***

### Why is swirl not asking me for my Coursera credentials when I complete a lesson?

You must have an old version of swirl. See the answer to [this question](https://github.com/swirldev/swirl/wiki/Coursera-FAQ#why-am-i-getting-an-old-version-of-swirl-even-though-i-followed-the-instructions-for-installing-the-most-recent-version).

***

### Why am I not able to install the R Programming course from swirl?

You are probably getting a message like this:

```
| Sorry, but I'm unable to fetch ‘R Programming: The basics of
| programming in R’ right now. Are you sure you have an internet
| connection? If so, would you like to try again or visit the course
| repository for instructions on how to install a course manually? Type 0
| to exit.
```

If you are sure that your internet connection is working (it must be if you're here!), then you are probably behind a firewall or connected through a proxy server. 

If you're on a work computer, sometimes the easiest solution is to try again from a personal computer. Otherwise, you can install the course manually by following the instructions [here](https://github.com/swirldev/swirl_courses#install-and-run-a-course-manually).

***

### I'm running Linux and can't get swirl to work correctly. What am I doing wrong?

Check out our [Installing swirl on Linux](https://github.com/swirldev/swirl/wiki/Installing-swirl-on-Linux) page.

***

### What is my Course ID?

After completing each swirl lesson, you'll be prompted for your Course ID. This helps us identify which session of the course you are enrolled in so that you get proper credit for your work.

**For example**, if your course website is https://class.coursera.org/rprog-003, then your Course ID is `rprog-003`.

![Course ID](https://dl.dropboxusercontent.com/u/14555519/Screenshot%202014-04-29%2013.48.28.png)

***

### Where can I find my Submission Password?

Your submission password is different from the password that you use to log in to the Coursera website. It can be found at the top of the Programming Assignments page.

![Submission password](https://dl.dropboxusercontent.com/u/14555519/Screenshot%202014-04-29%2013.51.13.png)

***

### I have some ideas for how to make swirl even better. Who should I tell?

Please follow the instructions here for making suggestions: http://swirlstats.com/help.html

***

### Where can I find more information about swirl?

Check out our website: http://swirlstats.com

***

### I found a typo in one of the swirl lessons. Where should I report it?

Please create a [New Issue](https://github.com/swirldev/swirl_courses/issues/new) over at our [course repository](https://github.com/swirldev/swirl_courses) and provide the following information:

- Course name
- Lesson name
- The text containing the typo (copy and paste)
- A brief description of the typo

Thanks for letting us know!

***

### When I install swirl, R tells me that it's not available for R 3.0.x. What should I do?

swirl requires R version 3.0.2 or later. You can check your R version by typing `R.version.string` at the R prompt. If you have an older version of R, then please [update it](http://cran.rstudio.com/) and reinstall swirl.

***

### Why is swirl running very slowly?

A cluttered workspace can cause swirl to run slowly. Before you start swirl, please clear your workspace with `rm(list=ls())`. If swirl still runs slowly, you may want to close other applications that you have open in the background.

***

### Why am I not getting any points for swirl lessons I've submitted?

Make sure you submitted before the deadline. All deadlines are listed on the Programming Assignments page. 

If you submitted before the deadline, then you probably skipped more than one question per lesson. swirl should have warned you of this when you tried to submit:

```
| I'll try to tell Coursera you've completed this lesson now.

| You skipped too many questions! You'll need to complete this lesson
| again if you'd like to receive credit. Please don't skip more than one
| question next time.

| You've reached the end of this lesson! Returning to the main menu...
```