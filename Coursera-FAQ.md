### 1. Automatic submission failed. How do I submit manually?

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

### 2. I'm running Linux and can't install swirl. What am I doing wrong?

### 3. What is my Course ID?

After completing each swirl lesson, you'll be prompted for your Course ID. This helps us identify which session of the course you are enrolled in so that you get proper credit for your work.

**For example**, if your course website is https://class.coursera.org/rprog-003, then your Course ID is `rprog-003`.

![Course ID](https://dl.dropboxusercontent.com/u/14555519/Screenshot%202014-04-29%2013.48.28.png)

### 4. Where can I find my Submission Password?

Your submission password is different from the password that you use to log in to the Coursera website. It can be found at the top of the Programming Assignments page.

![Submission password](https://dl.dropboxusercontent.com/u/14555519/Screenshot%202014-04-29%2013.51.13.png)

### 5. I have some ideas for how to make swirl even better. Who should I tell?

### 6. Where can I find more information about swirl?

Check out our website: http://swirlstats.com

### 7. I found a typo in one of the swirl lessons. Where should I report it?

Please create a New Issue on our Course Repository page. [NEED MORE INFO HERE]

### 8. When I install swirl, R tells me that it's not available for R 3.0.x. What should I do?

swirl requires R version 3.0.2 or later. You can check your R version by typing `sessionInfo()` at the R prompt. If you have an older version of R, then please update it and reinstall swirl.

### 9. Swirl is running very slowly. What should I do?

Having a cluttered workspace can cause swirl to run slowly. Before you start swirl, please clear your workspace with `rm(list=ls())`. If swirl still runs slowly, you may want to close some other applications that you have open in the background.

### 10. Something about firewalls, proxies, work computers, etc...

### 11. Warning: cannot remove prior installation of package ‘RCurl’ - Run as administrator