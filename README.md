## Conan package recipe for [*matroska*](https://github.com/Matroska-Org/libmatroska)

a C++ libary to parse matroska files

The packages generated with this **conanfile** can be found on [CampAR](https://conan.campar.in.tum.de/artifactory/webapp/#/home).


## Issues


## For Users

### Basic setup

    $ conan install matroska/1.6.2@camposs/stable

### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*

    [requires]
    matroska/1.6.2@camposs/stable

    [generators]
    cmake

Complete the installation of requirements for your project running:

    $ mkdir build && cd build && conan install ..

Note: It is recommended that you run conan install from a build directory and not the root of the project directory.  This is because conan generates *conanbuildinfo* files specific to a single build configuration which by default comes from an autodetected default profile located in ~/.conan/profiles/default .  If you pass different build configuration options to conan install, it will generate different *conanbuildinfo* files.  Thus, they should not be added to the root of the project, nor committed to git.


## Build and package

The following command both runs all the steps of the conan file, and publishes the package to the local system cache.  This includes downloading dependencies from "build_requires" and "requires" , and then running the build() method.

    $ conan create . camposs/stable


## Add Remote

    $ conan remote add camposs "https://conan.campar.in.tum.de/api/conan/conan-camposs"


## Conan Recipe License

NOTE: The conan recipe license applies only to the files of this recipe, which can be used to build and package matroska.
It does *not* in any way apply or is related to the actual software being packaged.

[MIT](https://github.com/ulricheck/conan-matroska/blob/stable/1.6.2/LICENSE.md)
