***

This page lists all of the most common errors and warnings related to installing and using the swirl R package. For each, we provide advice on what might be going wrong and how to fix the problem you're experiencing.

***

### Number 1:

```
> library(swirl)
Error in library(swirl) : there is no package called 'swirl'
```

Did you install swirl with `install.packages("swirl")`? If so, then something went wrong with installation. There are a few reasons this might occur. 

* Do you have R version 3.0.2 or later? This is required for the most recent version of swirl.
* Are you behind a firewall or proxy server at work? If you have access to a personal computer, that's often the easiest fix.
* Do you have full permissions on your computer? Again, using a personal computer may be your best bet.

***

### Number 2

```
> swirl()
Error: could not find function "swirl"
```

Did you load swirl with `library(swirl)`? The package must be loaded in order to access the `swirl()` function.

***

### Number 3

```
> install.packages("swirl")
Warning in install.packages :
  package ‘swirl’ is not available (for R version 3.0.1)
```

You must have R version 3.0.2 or later in order to get the most recent version of swirl. If you have an older version of R, you must update it before installing swirl.

***

### Number 4

```
> install.packages("swirl")
Warning message:
In getDependencies(pkgs, dependencies, available, lib) :
  package 'swirl' is not available (for R version 2.14.1)
```

This is the same problem as Number 3 above.

***

### Number 5

```
> install_from_swirl("R_Programming")
Error in function (type, msg, asError = TRUE)  : couldn't connect to host
```

This means your computer is not able to download a course from the internet. The most common cause of this is connecting through a firewall or proxy server. If you're on a work computer, you may want to try installing swirl on a personal computer. Otherwise, you can install courses manually by following [these instructions](https://github.com/swirldev/swirl_courses#install-and-run-a-course-manually).

***

### Number 6

```
> install_from_swirl("R_Programming")
Error in function (type, msg, asError = TRUE)  : 
  Failed to connect to <IP_Address>: Network is unreachable
```

Make sure you have an internet connection. If you do, then this is probably similar to Number 5.

***

### Number 7

```
> library(swirl)
Error in loadNamespace(j <- i[[1L]], c(lib.loc, .libPaths()), versionCheck = vI[[j]]) : 
  there is no package called ‘<package_name>’
```

For some reason, your computer is not able to load one of the packages that swirl depends on. This error is usually symptomatic of permissions issues on a work computer. You should try installing swirl on a personal computer if you have one.

***

### Number 8

```
> install.packages("swirl")

[...skipping output to save space...]

* installing *source* package ‘RCurl’ ...
** package ‘RCurl’ successfully unpacked and MD5 sums checked
checking for curl-config... no
Cannot find curl-config
ERROR: configuration failed for package ‘RCurl’
* removing ‘/home/ga/R/x86_64-pc-linux-gnu-library/3.1/RCurl’
ERROR: dependency ‘RCurl’ is not available for package ‘httr’
* removing ‘/home/ga/R/x86_64-pc-linux-gnu-library/3.1/httr’
ERROR: dependencies ‘httr’, ‘RCurl’ are not available for package ‘swirl’
* removing ‘/home/ga/R/x86_64-pc-linux-gnu-library/3.1/swirl’

The downloaded source packages are in
    ‘/tmp/RtmpvK6nyw/downloaded_packages’
Warning messages:
1: In install.packages("swirl") :
  installation of package ‘RCurl’ had non-zero exit status
2: In install.packages("swirl") :
  installation of package ‘httr’ had non-zero exit status
3: In install.packages("swirl") :
  installation of package ‘swirl’ had non-zero exit status
```

swirl uses the RCurl package to download courses from the internet. RCurl requires certain system level software to be installed. Most of the time, it's there already, but sometimes (mainly on Linux) it's not. Visit our [Installing swirl on Linux](https://github.com/swirldev/swirl/wiki/Installing-swirl-on-Linux) page for help.

***

### Number 9

```
> install.packages("swirl")

[...skipping output to save space...]

Warning: cannot remove prior installation of package ‘RCurl’
```

This is symptomatic of permission restrictions, most likely on a work computer. Please try installing swirl on a personal computer or have a friendly chat with your computer person to find a workaround.

***

### Number 10

```
Error in file(con, "w") : cannot open the connection
In addition: Warning message:
In file(con, "w") :
  cannot open file 'rprog-005_Basic_Building_Blocks.txt': Permission denied
```

Anytime you see `Permission denied`, it probably means that you don't have full file permissions on your computer. If you are using Windows, you may need to right-click R/RStudio and select "Run as administrator". If you are on a work/school computer, you may need to try using swirl from a personal computer or talk to your sys admin person.