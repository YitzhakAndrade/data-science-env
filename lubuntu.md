# Set up R environment in Lubuntu

## Download links:
- [R Studio](
https://www.rstudio.com/products/rstudio/download/#download)
- [Anaconda](https://www.continuum.io/downloads#linux)

## Video
[YouTube](https://youtu.be/gER-SGaIsu4)

## Install R

```bash
sudo leafpad /etc/apt/sources.list
```
deb http://cran.rstudio.com/bin/linux/ubuntu precise/

```bash
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E084DAB9
sudo add-apt-repository ppa:marutter/rdev
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install libssl-dev
sudo apt-get install libcurl4-openssl-dev
sudo apt-get install r-base
R
```

## Install devtools

```R
version
install.packages("httr")
install.packages("devtools", dependencies = TRUE)
packageVersion("devtools")
library(devtools)
find_rtools()
```

## Install R Studio

```bash
sudo leafpad /etc/apt/sources.list
```
deb http://httpredir.debian.org/debian jessie main


```bash
sudo leafpad /etc/apt/preferences.d/01_release
```

```text
Package: *
Pin: release o=Debian,a=unstable
Pin-Priority: 600

Package: *
Pin: release o=Debian,n=jessie
Pin-Priority: 10
```

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install libjpeg62
sudo apt-get install libgstreamer0.10-0
sudo apt-get install libgstreamer-plugins-base0.10-0
sudo dpkg -i rstudio-1.0.136-amd64.deb
```

## Install Anaconda

```bash
sudo bash Anaconda3-4.3.1-Linux-x86_64.sh
```

## Source:
- [Installing latest version of R-base](http://askubuntu.com/questions/218708/installing-latest-version-of-r-base)
- [RStudio installation failure under Debian sid: libgstreamer dependency problems](http://stackoverflow.com/questions/37550993/rstudio-installation-failure-under-debian-sid-libgstreamer-dependency-problems)


## Other useful links:
- [R Installation and Administration](https://cran.r-project.org/doc/manuals/r-release/R-admin.html)
