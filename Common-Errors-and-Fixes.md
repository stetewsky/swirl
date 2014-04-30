```
> library(swirl)
Error in library(swirl) : there is no package called 'swirl'
```


```
> swirl()
Error: could not find function "swirl"
```

```
Warning in install.packages :
  package ‘swirl’ is not available (for R version 3.0.1)
```

```
> install_from_swirl("R_Programming")
Error in function (type, msg, asError = TRUE)  : couldn't connect to host
```

```
> install_from_swirl("R_Programming")
Error in function (type, msg, asError = TRUE)  : 
  Failed to connect to <IP_Address>: Network is unreachable
```

```
> library(swirl)
Error in loadNamespace(j <- i[[1L]], c(lib.loc, .libPaths()), versionCheck = vI[[j]]) : 
  there is no package called ‘RCurl’
```


```
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