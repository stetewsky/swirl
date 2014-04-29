## Swirl installation for Linux Mint 16

Installation for other distributions in the Debian family should be similar.

1. Install build-essential (needed by gcc to compile Rpackages containing C/C++ code)
 * sudo apt-get install build-essential
2. Install curl and libcurl4-openssl-dev (which will be needed for RCurl)
 * sudo apt-get install curl
 * sudo apt-get install libcurl4-openssl-dev
3. Install R
 * sudo apt-get install r-base
4. Install [RStudio](http://www.rstudio.com/ide/download/desktop) if you are going to use it.
 * http://www.rstudio.com/ide/download/desktop
5. Install swirl from the R prompt
 * install.packages("swirl")
 * or install from RStudio’s graphical interface. Be sure that install dependencies is checked.

## Swirl installation from source package
### --Courtesy Naseeruddin

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

