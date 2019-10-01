## cmake, catch c++ boilerplate

[![Build Status](https://img.shields.io/travis/linuxenko/cccpp-boilerplate.svg?style=flat-square)](https://travis-ci.org/linuxenko/cccpp-boilerplate)

Most simple and robust c++ boilerplate for `cmake` with `catch` based tests.

### Why ?

There are lots of broken, misconfigured boilerplates. The worst part is dependencies which does not suite my needs.
It is the reason I've created another boilerplate and share it with you.

### Installation

1. Clone repository with:

```
git clone https://github.com/linuxenko/cccpp-boilerplate.git
```

2. Dependencies ! I'm sure you have installed `cmake` and `catch` on your system already, if not:

```
sudo apt install g++5 cmake catch
```

### Make the project

Lets build the boilerplate (empty) project

```
> mkdir build
> cd build
> cmake ../
> make
```

### Make tests

```
> make Test
```

### Automatically rebuild project and run tests

There are many different ways to watch filesystem changes, I prefer tools such as `rerun`.
To watch, build and run tests for every file change:

```
> cd build
> rerun -d ../src -p "**/*.cpp" "make ; make Test"
```

### License

Unlicensed, free for everyone :) 
