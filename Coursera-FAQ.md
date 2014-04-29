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

### Why am I not able to install the swirl R package?

Please do everything on this checklist:

- Make sure you have R version 3.0.2 or later
```
sessionInfo()
```
- If you are running Linux, following [these instructions](https://github.com/swirldev/swirl/wiki/Installing-swirl-on-Linux)
- Install the most recent version of swirl
```
install.packages("swirl")
```
- Check that you actually got the most recent version of swirl
```
packageVersion("swirl")
```

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

If you're on a work computer, sometimes the easiest solution is to try again from a personal computer. Otherwise, you can install the course manually by following the special instructions for Linux users below.

***

### I'm running Linux and can't install swirl. What am I doing wrong?

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

Please create a New Issue on our Course Repository page. [NEED MORE INFO HERE]

***

### When I install swirl, R tells me that it's not available for R 3.0.x. What should I do?

swirl requires R version 3.0.2 or later. You can check your R version by typing `sessionInfo()` at the R prompt. If you have an older version of R, then please update it and reinstall swirl.

***

### Why is swirl running very slowly?

Having a cluttered workspace can cause swirl to run slowly. Before you start swirl, please clear your workspace with `rm(list=ls())`. If swirl still runs slowly, you may want to close some other applications that you have open in the background.

***

### When I install swirl, I get a warning that says `cannot remove prior installation of package ‘RCurl’. What should I do?

[RUN R/RSTUDIO AS ADMINISTRATOR...]

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