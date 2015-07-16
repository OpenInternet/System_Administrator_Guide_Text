# Guide for System Administrators in At‐Risk Organizations

## License

The **Guide for System Administrators in At‐Risk Organizations** is available under a Creative Commons Attribution-NonCommercial 3.0 Unported (CC BY-NC 3.0) License

The guide may be used and shared for educational, non-commercial, not-for-profit purposes, with attribution to Internews. Users are free to modify and distribute content under conditions listed in the license.

# Building the System Administrator Guide PDF

### Install Git

```
sudo apt-get install git
```

### Install the [Documentation Builder](https://github.com/OpenInternet/Documentation-Builder.git)

[Use the installation instructions found here.](https://github.com/OpenInternet/Documentation-Builder/blob/master/docs/INSTALL.md)

### Download the [System Administrator Guide Text](https://github.com/OpenInternet/System_Administrator_Guide_Text)

```
git clone https://github.com/OpenInternet/System_Administrator_Guide_Text.git
```
### Download and Install the [System Administrator Guide Theme Templates](https://github.com/OpenInternet/System_Administrator_Guide_Templates)

```
git clone https://github.com/OpenInternet/System_Administrator_Guide_Templates.git
cd System_Administrator_Guide_Templates
./install
cd ..
```

### Create the System Administrator Guide

```
cd /path/to/documentation/builder/
./builddoc  -i path/to/System_Administrator_Guide_Text/en -t /path/to/System_Administrator_Guide_Templates/ -o output_filename.pdf
```
