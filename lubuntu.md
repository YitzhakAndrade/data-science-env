# Set up Data Science environment in Lubuntu

- Anaconda using Python 3 and creating a alternative Python 2.7 environment.
- Can works in Ubuntu and Mint too.

## Download links:
- [R Studio](
https://www.rstudio.com/products/rstudio/download/#download)
- [Anaconda](https://www.continuum.io/downloads#linux)

## Video
[YouTube](https://youtu.be/1xbU9BmINak)

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

## Install R devtools

```R
R
version
install.packages("httr")
install.packages("devtools", dependencies = TRUE)
packageVersion("devtools")
library(devtools)
find_rtools()
```

## Install R Studio

If you're using Ubuntu or Mint, only install the package:

```bash
sudo dpkg -i rstudio-1.0.136-amd64.deb
```

If you're using Lubuntu, you may need to install some others packages before install R Studio:

```bash
sudo leafpad /etc/apt/sources.list
```

Add the line bellow at the end of file:
```text
# /etc/apt/sources.list
deb http://httpredir.debian.org/debian jessie main
```

```bash
sudo leafpad /etc/apt/preferences.d/01_release
```

Add the lines bellow at the end of file:
```text
# /etc/apt/preferences.d/01_release

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

## Install Anaconda Navigator

```bash
cd /usr/anaconda3
sudo chown john * -R
conda install anaconda-navigator
```

## Create Python 2.7 environment

```bash
conda create -n py27 python=2.7 anaconda

#
# To activate this environment, use:
# > source activate py27
#
# To deactivate this environment, use:
# > source deactivate py27
#
```



## Source:
- [Installing latest version of R-base](http://askubuntu.com/questions/218708/installing-latest-version-of-r-base)
- [RStudio installation failure under Debian sid: libgstreamer dependency problems](http://stackoverflow.com/questions/37550993/rstudio-installation-failure-under-debian-sid-libgstreamer-dependency-problems)
- [Managing Python - Conda documentation](https://conda.io/docs/py2or3.html)

## Other useful links:
- [R Installation and Administration](https://cran.r-project.org/doc/manuals/r-release/R-admin.html)
