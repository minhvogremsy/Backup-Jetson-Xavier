# OpenTLD_interface Example
This is a C++ implementation of OpenTLD that was originally published in MATLAB by Zdenek Kalal. OpenTLD is used for tracking objects in video streams. What makes this algorithm outstanding is that it does not make use of any training data.  This implementation is use Opencv 3.4.6 and GStreamer pipeline to get data return from camera and create an appsink which process it with OpenTLD.

## Compiling OpenTLD programs
Go into the folder OpenTLD and type: 
```bash
$ cd $OpenTLD
$ mkdir ../build
$ cd ../build
$ cmake ..
```

If it is fine proceed with the compilation (Use nproc to know the number of cpu cores):
```bash
$ make -j${nproc} 
$ ./bin/main
```

# Usage
## Keyboard shortcuts

* `q` quit
* `c` clear object and stop tracking
* `r` clear model, let user reinit tracking
## Samples
### main_gstreamer.cpp
* Remember that you can use the `w` and `h` to init width and height of bounding box for size of object (the default is w = 64 and h = 64).

# Dependencies
* OpenCV 3.4.6
* CMake
* libconfig++ (optional)
* Qt5 (optional)
