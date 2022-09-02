---
layout: page
title: LAPACK Tutorial
permalink: /academics/lapack/
exclude: true
---

This is a tutorial for using [LAPACK](https://en.wikipedia.org/wiki/LAPACK) library. 
LAPACK is a standard library for high-performance numerical linear algebra and is written in `Fortran`. 
However, I will be writing my code in `c++`. 
There are `c++` interfaces that allow one to call LAPACK functions in a `c++` file.  
The reason I am interested in this library is to efficiently calculate the band-structure of semiconductor heterostructures. 
This requires various linear algebra algorithms for finding eigenvalues and eigenvectors of Hermitian matrices as well as solving for linear system of differential equations.

## Hardware specifications 
I have included my hardware specifications here for the sake of reproducability and thoroughness. 
- Machine: MacBook Pro (15-inch, 2019)
- CPU: 2.6 GHz 6-Core Intel Core i7
- OS: macOS Monterey Version 12.5.1

## Install C++ compiler
I will be using the C++ compiler that is bundled with Xcode. 
So, I would just need to install Xcode. 
Use this command to check if Xcode has installed correctly:
```bash
xcode-select -p
```
If so, you should see the following:
```bash
/Applications/Xcode.app/Contents/Developer
```
Now, check the version of `g++`: 
```bash
g++ --version
```
You should be getting something like: 
```bash 
Apple clang version 13.1.6 (clang-1316.0.21.2.5)
Target: x86_64-apple-darwin21.6.0
Thread model: posix
InstalledDir: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin
```

## Set up LAPACK
I am going to use the bundled version of LAPACK that comes automatically with the Accelerate framework on Apple computers. 
The only thing you would need to do is include the Accelerate header file as follows:
```cpp
#include <Accelerate/Accelerate.h>
```

## Useful LAPACK functions 
Since this is not an exhaustive tutorial, I will only show how to use some of the more useful LAPACK functions for my specific problem. 