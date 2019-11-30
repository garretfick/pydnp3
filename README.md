# pyopendnp3

This project is a minor fork of the great
[pydnp3](https://github.com/ChargePoint/pydnp3) library, which provides Python
bindings for OpenDNP3.

Why fork? Because pydnp3 only provides pip-friendly wheels for Python 2
and Python 2.7 has reached end of life. This fork aims to provide pip-friendly
wheels for Python 3 available on PyPI.

While the name of the project is pyopendnp3, module names are unchanged and
thus code that worked with pydnp3 should work with no changes.

This project currently produces wheels for the following platforms:

* Windows
  * Python 3.5 x86-64
  * Python 3.6 x86-64
  * Python 3.7 x86-64
  * Python 3.8 x86-64

The remainder of this README is reproduced verbatim from pydnp3.

Python bindings for the [opendnp3](https://github.com/automatak/dnp3) library,  an open source
implementation of the [DNP3](http://ww.dnp.org) protocol stack written in C++14.

Note:  This is a work in progress.  See [Issues](http://github.com/Kisensum/pydnp3/issues) for things we know about and feel free to add your own.

**Supported Platforms:** Linux, MacOS

## Dependencies
To build the library from source, you must have:

* A toolchain with a C++14 compiler
* CMake >= 2.8.12 (https://cmake.org/download/)

This repository includes two repositories as submodules (under `deps/`):

* dnp3 (https://github.com/automatak/dnp3)
* pybind11 (https://github.com/Kisensum/pybind11) - This is a fork containing a minor patch
required to compile some of the pydnp3 wrapper code. It will be replaced with pybind11 proper
when the issue is resolved.

## Build & Install
At the moment, this library must be built from source:
```
    $ clone --recursive http://github.com/Kisensum/pydnp3
    $ cd pydnp3
    $ python setup.py install
```


## Documentation

pydnp3 is a thin wrapper around most all of the opendnp3 classes.  Documentation for the opendnp3
classes is available at [automatak](https://www.automatak.com/opendnp3/#documentation).

Use python's help to discover the available wrapper classes and functions.  For example,

```
> import pydnp3
> help (pydnp3.opendnp3)
Help on module pydnp3.opendnp3 in pydnp3:

NAME
    pydnp3.opendnp3 - Bindings for opendnp3 namespace

FILE
    (built-in)

CLASSES
    pybind11_builtins.pybind11_object(__builtin__.object)
        AnalogCommandEvent
        AnalogInfo
            AnalogSpec
...
```

