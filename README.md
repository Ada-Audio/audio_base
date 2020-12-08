Base for Audio Applications using Ada
=====================================

**Version 1.0.0**

![GNAT 7 on Ubuntu 18.04](https://github.com/Ada-Audio/audio_base/workflows/GNAT%207%20on%20Ubuntu%2018.04/badge.svg)
![GNAT 8 on Ubuntu 20.04](https://github.com/Ada-Audio/audio_base/workflows/GNAT%208%20on%20Ubuntu%2020.04/badge.svg)
![GNAT 9 on Ubuntu 20.04](https://github.com/Ada-Audio/audio_base/workflows/GNAT%209%20on%20Ubuntu%2020.04/badge.svg)
![GNAT 10 on Ubuntu 20.04](https://github.com/Ada-Audio/audio_base/workflows/GNAT%2010%20on%20Ubuntu%2020.04/badge.svg)
![GNAT Community 2020 on Ubuntu 20.04](https://github.com/Ada-Audio/audio_base/workflows/GNAT%20Community%202020%20on%20Ubuntu%2020.04/badge.svg)


Introduction
------------

This Library contains basic packages for audio applications.


License & Copyright
-------------------

As indicated in the [LICENSE](LICENSE) file, this Package is available "as is"
under MIT License. Please refer to that file for all licensing conditions.
Unless stated otherwise, the copyright is held by Gustavo A. Hoffmann.


Supported Platforms
-------------------

This Package has been tested with following compilers and platforms:

- GNAT FSF 7, 8, 9 and 10 for Linux;
- GNAT Community 2020 for Linux, Windows and macOS.


Setting Up the Library
----------------------

### Using ALIRE

You can retrieve this Library as a crate from
[ALIRE](https://alire.ada.dev) (the Ada LIbrary REpository):

```sh
alr get audio_base
```

Then, you can build the Library (as a standalone library) with
[ALIRE](https://alire.ada.dev) using the following command:

```sh
cd audio_base*

alr build
```

### Cloning the source-code

Alternatively, you can clone the source-code of the Library and its
dependencies using these commands from the root directory of your project:

```sh
mkdir deps

(cd deps && git clone https://github.com/Ada-Audio/audio_base )
```

Then, you have to include the Library in your GPRbuild project by adding
the following line:

```
with "audio_base.gpr";
```

You can use GPRbuild to build your project with the Library. Don't forget
to set the path to the GPRbuild project file using the environment variable
`GPR_PROJECT_PATH`:


```sh
# Set path to audio_base and wavefiles
export GPR_PROJECT_PATH="$(cd deps/audio_base && pwd)"

gprbuild
```


Using the Library
-----------------

This Library serves as a starting point for creating child packages based on
the `Audio` or the `Audio.RIFF` packages.
