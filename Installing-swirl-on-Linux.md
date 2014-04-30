### Ubuntu (tested on 12.04 LTS - "Precise")

#### 1. Install the most recent version of R. If you have R installed already, go to #2.

**IMPORTANT: In the first line below, `precise/` should be replaced with the version of Ubuntu you are using. Other examples: `trusty/`, `saucy/`, `quantal/`, `lucid/`. If you're not sure which version you have, type `cat /etc/*release` at the command line.**

Official source: http://cran.r-project.org/bin/linux/ubuntu/README

```
$ sudo sh -c 'echo "deb http://cran.rstudio.com/bin/linux/ubuntu precise/" >> /etc/apt/sources.list'
$ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E084DAB9
$ sudo apt-get update
$ sudo apt-get install r-base-dev
```

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
> swirl()
```

**NOTE: If you upgrading from an earlier version of R, you may need to do `install.packages("codetools")` before installing swirl.**

***

### Linux Mint 16

#### 1. Install build-essential (needed by gcc to compile R packages containing C/C++ code)

```
$ sudo apt-get install build-essential
```

#### 2. Install curl and libcurl4-openssl-dev (which will be needed for RCurl)

``` 
$ sudo apt-get install curl
$ sudo apt-get install libcurl4-openssl-dev
````

#### 3. Install R

```
$ sudo apt-get install r-base-dev
```

#### 4. Install RStudio (optional, but recommended).

Download from http://www.rstudio.com/ide/download/desktop.

#### 5. Install swirl from the R prompt

```
> install.packages("swirl")
```

***

### Swirl installation from source package
#### --Courtesy Naseeruddin

1. Download tar.gz file from http://cran.rstudio.com/src/base/R-3/R-3.1.0.tar.gz
2. change the directory where the tar file is and then untar file using the command   tar -zxvf R 3.1.0.targz
3. ./configure
4. make
5. sudo make install
6. cd bin
7. ./R
(Note: During the configure, it checks for dependencies of the libraries it needs. so if these dependencies are not met, it will take extra effort to install those dependencies. They may include libcurl4-openssl-dev, etc.)

This version of R will be 3.1.0 (Now you can add this working directory to your path variable to access R from anywhere.)

Now follow the steps to install swirl

1. install.packages("swirl")
2. library(swirl)
3. swirl()

***

### Other Resources

**Often, the most challenging part of getting swirl to work on Linux is getting a recent version of R. We've found this blog post to be a helpful resource for installing R on a variety of Linux platforms: http://www.jason-french.com/blog/2013/03/11/installing-r-in-linux/**