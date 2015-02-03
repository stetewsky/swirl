swirl and its dependencies require R version 3.0.2 or later as well as a recent version of libcurl. This page is our attempt to collect any information that might be helpful to Linux users wanting to install swirl.

***

### Ubuntu and its derivatives

These instructions have been successfully tested on:
- Ubuntu 12.04 LTS (Precise Pangolin)
- Linux Mint 16 (Petra)

#### 1. Install the most recent version of R. If you have R installed already, go to #2.

Official source: http://cran.r-project.org/bin/linux/ubuntu/README

**IMPORTANT: In the first line below, `precise/` should be replaced with the version of Ubuntu you are using. Other examples: `trusty/`, `saucy/`, `quantal/`, `lucid/`. If you're not sure which version you have, type `cat /etc/*release` at the command line.**

```
$ sudo sh -c 'echo "deb http://cran.rstudio.com/bin/linux/ubuntu precise/" >> /etc/apt/sources.list'
$ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E084DAB9
$ sudo apt-get update
$ sudo apt-get install r-base-dev
```
**NOTE**

Most modern Linux distros recommend you not edit `/etc/apt/sources.list` directly and rather place any additions you want to outlive a package update in the `/etc/apt/sources.list.d` directory. With that in mind a best-practices alternative to the command above would be:
```
$ sudo sh -c 'echo "deb http://cran.rstudio.com/bin/linux/ubuntu precise/" >> /etc/apt/sources.list.d/cran.list'
```
Note also that using either of these instructions on a more modern distribution (e.g. Ubuntu 14.10, and probably 14.04) breaks the install, since the package at that source depends on libtiff4, but this has been removed (superseded by libtiff5). Happily, users can (and should) skip that step entirely, since a compatible package (R 3.1.1) is already included in that distribution.

PS. Thanks [Charl](https://github.com/charl)

#### 2. Confirm that you have R version 3.0.2 or later. If not, return to #1.

```
$ R --version
```

#### 3. Get RStudio (optional, but recommended).

Download from http://www.rstudio.com/ide/download/desktop.

#### 4. Install libcurl.

This is [required](http://www.omegahat.org/RCurl/FAQ.html) for the RCurl package, which swirl uses to download courses from the internet.

```
$ sudo apt-get install libcurl4-openssl-dev
```

#### 5. From R or RStudio, install and run swirl.

```
> install.packages("swirl")
> library(swirl)
> swirl()
```

**NOTE: If you upgrading from an earlier version of R, you may need to do `install.packages("codetools")` before installing swirl.**

***

### Other Resources

- Often, the most challenging part of getting swirl to work on Linux is getting a recent version of R. We've found [this blog post](http://www.jason-french.com/blog/2013/03/11/installing-r-in-linux/) to be a helpful resource for installing up-to-date versions of R on a variety of Linux platforms.

- Official R FAQ: [Are there Unix-like binaries for R?](http://cran.r-project.org/doc/FAQ/R-FAQ.html#Are-there-Unix_002dlike-binaries-for-R_003f)

- Official R installation docs for various Linux distributions:
  - Debian: http://cran.r-project.org/bin/linux/debian/
  - openSUSE: http://cran.r-project.org/bin/linux/suse/README.html
  - Ubuntu: http://cran.r-project.org/bin/linux/ubuntu/README.html

- Official R Installation and Administration manual on building R from source: [Installing R under Unix-alikes](http://cran.r-project.org/doc/manuals/R-admin.html#Installing-R-under-Unix_002dalikes).

- Download page for curl and libcurl: http://curl.haxx.se/download.html