# Instructions for build Firefox on Windows #

Recently, I needed to build the firefox browser from the source. I followed the officail tutorials from [Building Firefox for Windows](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions/Windows_Prerequisites), but it's partly userful. There are other problems that not mentioned in the tutoial will block your building, so I wrote this note to fill holes. By the way, the majority of the offical sites will not be repeated here, I just outline some important points.

**Therefore, the original offical tutorial from [Building Firefox for Windows](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Build_Instructions/Windows_Prerequisites) have to be read firstly!**

# The Essential prerequisites #

From the offical tutorial, we know that there are three software packages required for building Firefox:

1. Visual Studio 2017 or Visual Studio 2015, I strongly recommend the 2017's.
2. The Rust package from [Rust](https://rustup.rs/) .
3.  [MozillaBuild](https://ftp.mozilla.org/pub/mozilla.org/mozilla/libraries/win32/MozillaBuildSetup-Latest.exe).

# The Build Steps #

## Initialize the source code ##

- Prepare the source directory:

Following previous instructions and offical instructions, the MozilaBuild package is located at "C:\mozilla-build", then the build environment need to be done by double clicking "start-shell.bat". The unix-like terminal is showed, therefore the next commands can be run.

```bash
cd c:/
mkdir mozilla-source
cd mozilla-source
```

- Fetch the source code:

```bash
hg clone https://hg.mozilla.org/mozilla-central
```

## Before Building ##

Before running "mach build",  runing "mach bootstrap" is very helpful to initiate the build envirnment. But after running "bootstrap", we need to make choice like below:

```bash
$ mach bootstrap
mach bootstrap is not fully implemented in MozillaBuild

Please choose the version of Firefox you want to build:
1. Firefox for Desktop Artifact Mode
2. Firefox for Desktop
3. Firefox for Android Artifact Mode
4. Firefox for Android
```
After my own tries, the option 2 is better, what is the root cause I still don't investigate. Then follow prompts, you could choose yes or no, whatever. 

## Config the build system ##

There is a sample file whose name is "mozconfig" for configuring build located at "$(firefox_src_root)/browser/config/". We'd better copy it to the source root directory, then add some options to control build process.

- Copy the sample file into the srouce root directory:

```bash
cp browser/config/mozconfig .
```

Currently I only know how to modify this file to build the source for 64bit Windows, some other's options need more studies.

The build may fail if your machine is configured with the wrong architecture. If you want to build 64-bit Firefox, add the two lines below to your mozconfig file:

```bash
ac_add_options --target=x86_64-pc-mingw32
ac_add_options --host=x86_64-pc-mingw32 
```

If you have both Visual Studio 2015 and 2017 installed, the build system will default to using 2017. This can be overridden by adding the line below to your mozconfig file:

ac_add_options --with-visual-studio-version=2015

## Build the source ##

```bash
mach build
```

## During the process of building ##

After running "mach build", the checking routine will be launched firstly. The most important thing is that llvm-config is required, and the Windows binaries from LLVM offical site don't contain llvm-config! We must build for ourselves. The fucking tutorial don't mention this at all! And the version of LLVM source must be above 3.9.0, I have built the llvm and clang 4.0 successully, they are at [here](http://pan.baidu.com/s/1i4EzvN3) . The following section will show some tips on how to build llvm besides the offical doc, someone don't have interests on can skip.

### How to build llvm and clang on Windows 64 bits ###

Besides the tutorial from http://clang.llvm.org/get_started.html, I must use Cygwin64bit as the command interface and run

```bash
 cmake -G "Visual Studio 15 2017 Win64" -t host=x64 ..
```

This command will generate the vs's project file correctly!
 
### Set the llvm binary path to .bash_profile ###

Because the mozila build system uses unix-like terminal(MING32) to build on Windows, Setting path in .bash_profile under the user's diretory will work:

```bash
PATH=$PATH:c/llvm/Release/bin
```

With these actions to tackle problems during build process, we probabely build it successfully.

## Run the build ##

```bash
mach run
```

# Future topics #

Something more need to be investigated:

1. Making acquaintance with the source code, it's a huge project like OS, therefore researching the source code will be a long journy.
2. How to make the Windows install package from the source, I have known the package is constructed by nsis language, but no tutorials mention how to make the installer.
