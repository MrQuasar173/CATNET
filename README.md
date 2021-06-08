# CATnet
CATnet is a more desentralized web for a more modern age.

## User use
### Installation
CATnet uses the Meson build system, because quite simply, it is one of the best build systems for C++. But you're not here to find out why Meson is so awesome, you just want to build CATnet. To build CATnet, you must have Meson and Ninja installed on your system.  
If on Linux, just install your distros meson package, and ninja will be installed along side it. Same on Mac OS. On Windows, winget doesn't have a package for it. Please look up installation directions for Meson and Ninja on Windows. Or throw your Windows cursed hard drive in a bin. Either works.  
As of now, you do not need any libraries preinstalled because the C/C++ standard libraries (duh). However, since Google ProtoBuf takes a while to build, you can download a prebuilt binary from your package manager to speed up the build (the build scripts try to automatically detect it). The following is how to build CATnet.  
```bash
# Clone the repo if you haven't already
git clone https://github.com/ZincSoft/CATNET.git
cd CATNET

# Configure the project
meson build

# Build the project
cd build
ninja
```

### Use
Please run `catnetd --help` to get a help message. To launch the participant (run a whisker), use `catnetd participant`. In opposision, to run the registrar, use `catnetd registrar`.

## Software Development
### Usefull flags
During development of CATnet, you may wish these flags:
* `-l0`, enables all levels of logging. Please note that in the future, this may not be available in release builds.

### Building
The way to build CATnet is basically the same as how a regular user would, but instead of running `meson build` you run `meson build --buildtype=debug`

### Code Guidelines
In order to make CATnet easier to maintain and understand, we follow the [CppCoreGuidelines](http://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines). If you need to find out how to style a specific C++ feature, please use your browsers built in search function, or clone it onto your system and `find . | grep x`.
The first time you use a feature (even if it is trivial, such as function declaration), please look up the prefered way to use it in the guidelines.

### Git Workflow
Pretend the other people working on this code base are insane, have a shotgun, and know where you live. As such, please follow `WORKFLOW.MD`.

### Specification
[Here](https://docs.google.com/document/d/1t3FXJTDr-h4J9iPvzBLDdCKGJAukKruhrJjNaMWRgq0/edit?ts=5fc41d5f#heading=h.3bqhl2hpdgyy) is a link to our specifications document (Alpha).
