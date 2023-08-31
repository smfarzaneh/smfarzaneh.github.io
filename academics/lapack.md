---
layout: page
title: LAPACK Tutorial
permalink: /academics/lapack/
exclude: true
---

This is a tutorial for using the [LAPACK](https://en.wikipedia.org/wiki/LAPACK) library. 
LAPACK is a standard library for high-performance numerical linear algebra and is written in `Fortran`. 
However, there are `C++` interfaces that allow one to call LAPACK functions in a `C++` file.  
The reason I am interested in this library is to efficiently calculate the band-structure of semiconductor heterostructures. 
This requires various linear algebra algorithms for finding eigenvalues and eigenvectors of Hermitian matrices as well as solving for linear system of differential equations.
I will be writing my code in `C++`. 

## Hardware specifications 
I have included my hardware specifications here for the sake of reproducability and thoroughness. 
- Machine: MacBook Pro (15-inch, 2019)
- CPU: 2.6 GHz 6-Core Intel Core i7
- OS: macOS Monterey Version 12.5.1

## Install C++ compiler
I will be using the `C++` compiler that is bundled with `Xcode`. 
So, I would just need to install `Xcode`. 
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
I am going to use the bundled version of LAPACK that comes automatically with the [Accelerate](https://developer.apple.com/documentation/accelerate) framework on Apple computers. 
If you have `Xcode` installed you should be able to find the `Accelerate.h` header file somehwere inside `Xcode` directory: 
```bash
/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/System/Library/Frameworks/Accelerate.framework/Headers
```
The only thing you would need to do is include the Accelerate header file in your `C++` code as follows:
```c++
#include <Accelerate/Accelerate.h>
```

## Useful functions 
Since this is not an exhaustive tutorial, I will only show how to use some of the more useful LAPACK functions for my specific problem. 
You can find the complete documentation [online](https://netlib.org/lapack/index.html) or in the following book:
* Anderson, E., Bai, Z., Bischof, C., Blackford, L. S., Demmel, J., Dongarra, J., ... & Sorensen, D. (1999). LAPACK users' guide. Society for industrial and applied mathematics.  




