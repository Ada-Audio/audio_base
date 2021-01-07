Base Library for Audio Applications using Ada
=============================================

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

### Cloning the source-code

You can clone the source-code of the Library using these commands from the root
directory of your project:

```sh
mkdir deps

(cd deps && git clone https://github.com/Ada-Audio/audio_base )
```

Note that you can use the `--branch` option to retrieve a specific version —
for example: `--branch 1.0.0`.

### Integration with your project

This section describes how to manually integrate the Library into your GPRbuild
project. If you're using ALIRE, please refer to the next section.

You can include the Library in your GPRbuild project by adding the following
line:

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

### Using ALIRE

If you're using [ALIRE](https://alire.ada.dev) (the Ada LIbrary REpository),
this section shows how you can integrate the Library to your project using the
ALIRE environment. These are the prerequisites:

1. You have cloned the source-code of the Library using one of the methods
   described above.

2. You have initialized your project for ALIRE.

You can now integrate the Library to the ALIRE environment using this command:

```sh
alr with audio_base      --use $(cd deps/audio_base      && pwd)
```


Using the Library
-----------------

This Library serves as a starting point for creating child packages based on
the `Audio` or the `Audio.RIFF` packages.
