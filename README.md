# iOS_3D_Scanner
# Description
The first mobile 3D scanner for iOS.
Application to help building 3D models for better user experineces.
With this app you can capture 3D models of yourself, friends or family members and share the results afterwards.
This is a research project to explore the 3D  scan with free libraries. Feel free to use it for experiments, modify and 
adapt it to new devices and contribute new features or ideas.

This project has been developed in Objective C and Swift language.


## Demo 
https://drive.google.com/file/d/1JV31JDEigUFneveZ2wdAGNVl03qwEngv/view?usp=drivesdk

## Requirements
1. Xcode version > 10.0<br/>
2. PCL library(Visit http://www.pointclouds.org> <br/>
3. Cmake GUI


# Installation of PCL using Homebrew
## Prerequisites
You will need to have Homebrew installed. If you do not already have a Homebrew installation, see the Homebrew homepage for installation instructions.

The PCL formula is in the Homebrew official repositories. This will automatically install all necessary dependencies and provides options for controlling which parts of PCL are installed.<br/>
```sh
$ brew install pcl
$ brew options pcl
```

# Compiling and running the project
## Using command line CMake
Step 1
```sh
$ cd /PATH/TO/MY/GRAND/PROJECT
$ mkdir build
$ cd build
$ cmake ..
```


You will something like this<br/>
-- The C compiler identification is GNU<br/>
-- The CXX compiler identification is GNU<br/>
-- Check for working C compiler: /usr/bin/gcc<br/>
-- Check for working C compiler: /usr/bin/gcc -- works<br/>
-- Detecting C compiler ABI info<br/>
-- Detecting C compiler ABI info - done<br/>
-- Check for working CXX compiler: /usr/bin/c++<br/>
-- Check for working CXX compiler: /usr/bin/c++ -- works<br/>
-- Detecting CXX compiler ABI info<br/>
-- Detecting CXX compiler ABI info - done<br/><br/>
-- Found PCL_IO: /usr/local/lib/libpcl_io.so<br/>
-- Found PCL: /usr/local/lib/libpcl_io.so (Required is at least version "1.0")<br/>
-- Configuring done<br/>
-- Generating done<br/>
-- Build files have been written to: /PATH/TO/MY/GRAND/PROJECT/build<br/>

Step 2<br/>
```sh
$ make
```

You will something like this<br/>
Scanning dependencies of target pcd_write_test<br/>
[100%] Building CXX object<br/>
CMakeFiles/pcd_write_test.dir/pcd_write.cpp.o<br/>
Linking CXX executable pcd_write_test<br/>
[100%] Built target pcd_write_test<br/>

The project is now ready to test<br/>
 Step 3<br/>
 ```sh
 $ ./pcd_write_test
 ```
 
 Final result will be like this<br/>
 Saved 5 data points to test_pcd.pcd.<br/>
  0.352222 -0.151883 -0.106395<br/>
  -0.397406 -0.473106 0.292602<br/>
  -0.731898 0.667105 0.441304<br/>
  -0.734766 0.854581 -0.0361733<br/>
  -0.4607 -0.277468 -0.916762<br/>
