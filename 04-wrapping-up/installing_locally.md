
# Rstudio server

The RStudio you used for the workshop today is available as a public Amazon Machine Image (AMI). The machine ID is:

```coffee
ami-81b8f7e8
```

This means that you can use your own [personal Amazon account](https://console.aws.amazon.com/console/home) to launch an instance of this machine image at your convenience. We'll keep all the stable versions of rOpenSci packages and tools updated at all times. 

You will most likely just want to work locally on your copy of RStudio. In that case, you'll need the latest version of R (currently `3.0.1`) and [RStudio](http://www.rstudio.com/) for your platform. Then install the following packages:

```coffee  
# First install the devtools package since it will allow you to install packages directly from GitHub that haven't yet been submitted to CRAN.

install.packages("devtools")  
library(devtools)  
```

Next install:

```coffee  
# From CRAN  
install.packages("ggplot2", dependencies = TRUE)  
install.packages("dismo")  
install.packages("maptools")  
install.packages("knitr") # for reproducible documents  
install.packages("rgbif")  
install.packages("rplos")  
install.packages("rfisheries")  
install.packages("rfigshare")  
install.packages("taxize")  

# from GitHub
install_github("taxize_",  "ropensci")  
install_github("rWBclimate",  "ropensci")  
install_github("reml",  "ropensci", ref = "xxxxx")  
```



*Note: REML currently has dependencies that are not on CRAN. See [this page]() for instructions on how to install them from source. Once a stable version is ready, all dependencies will also be available and setup will be a lot simpler.*


