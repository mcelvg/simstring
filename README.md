SimString build for Java on OSX
===================

SimString is written by Naoaki Okazaki.
http://www.chokkan.org/software/simstring/


###sources

- simstring-1.0: http://www.chokkan.org/software/dist/simstring-1.0.tar.gz
- simstring-1.1: https://github.com/chokkan/simstring


###prerequisites

This build tested on Mac OS 10.9.5 with the following dependencies:

 * Java version 1.7+ (1.7.0_45 & 1.8.0_45)
 * SWIG version 3.0.2 configured with +pcre, compiled with clang++ [x86_64-apple-darwin13.4.0]
 * g++ version 4.2.1, specifically i686-apple-darwin11-g++-4.2.1 (GCC) 4.2.1 (Apple Inc. build 5666) (dot 3)

```sh
brew install swig
brew tap homebrew/versions
brew install apple-gcc42
```

N.B. SimString itself will build with the default compiler on OSX (clang++). The SWIG interface will not. The most recent version of g++ (Homebrew gcc 5.2.0) won't work either.

###build

```sh
git clone https://github.com/mcelvg/simstring.git
cd simstring
./configure
make
make install
```

Compile the SWIG interface for Java

```sh
cd swig/java
./prepare.sh --swig
make
```

###test SWIG interface

```sh
make sample
./run_sample.sh 
```

expected output:

```
Barack Hussein Obama II
James Gordon Brown

Barack Hussein Obama II
```

