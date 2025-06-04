## Compiling

### Dependencies

GMML2 is only supported on Linux. The following packages are required

* `cmake` (Version >= `3.13.4`)
* `g++` (Version >= `7.0`)
* `openmp`
* `make`
* `git`
* `libeigen3-dev` (Version >= `3.3.7`)

---
### Compiling

To compile, run the `make.sh` script in your GMML2 directory. To use more than one core, use the `-j` flag, e.g `./make.sh -j 8`.
For help with the script, run `./make.sh -h`

This will create the needed `cmake` files and will add the following directories within the `gmml2` directory:

* `lib` (Contains the `gmml2` shared object libary, `libgmml2.so`)
* `bin` (Contains executables for the programs provided by GMML2, as listed in the [index](index.md))
* `cmakeBuild` (Contains the `cmake` files, a `compile_commands.json` file to be used with tools of your choice, and all files contained within the directories listed above)

### Wrapping with Swig

Swig is a tool which can bridge C++ code to other languages such as Python.
Most linux distros have swig 4.0. Otherwise swig 4.0.2 must be installed from [their website](https://www.swig.org/download.html). 

Swig wrapping adds the following dependencies

* `python3.9` (Version `3.9.12`)
* `python3.9-dev` (Version `3.9.12`)
* `swig` (Version `4.0.2`)

In order to wrap with Swig, use the `-w` flag of the make script, e.g `./make.sh -w` 
