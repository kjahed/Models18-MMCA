## The Run-Time Service

In order for Papyrus-RT to be able to create executable applications, it needs not only needs the code generated from the model, but also a set of run-time services that implement the underlying "virtual machine" for the model. This run-time service (RTS) library provides the glue that connect sand enables the various constructs defined by UML-RT, such as messaging, time-related capabilities, dynamic structure control, and support for state machine driven behavior.

Out of the box, the [Papyrus-RT builds](https://github.com/kjahed/Models18-MMCA/blob/master/index.md#download-papyrus-r) hosted on this repository provides a pre-compiled version of this RTS library. However, it might happen that the included library is incompatible with the toolchain (compiler, etc..) installed on your system.

This tutorial will show you how you can build the RTS library using the toolchain on your machine.

## Building the RTS
This tutorial assumes that you have a [working C++ compiler](https://github.com/kjahed/Models18-MMCA/blob/master/index.md#prerequisite) installed on your system, and that you've already [downloaded](https://github.com/kjahed/Models18-MMCA/blob/master/index.md#download-papyrus-rt) and extracted the Papyrus-RT folder to some directory ```<INSTALL_DIR>```.

### On Linux
Simply open a terminal and navigate to the RTS directory within Papyrus-RT then run ```make```.
```
cd <INSTALL_DIR>/Papyrus-RT/plugins/org.eclipse.papyrusrt.rts_1.0.0.201810091347/umlrts
make
```

### On macOS
**IMPORTANT: make sure to open Papyrus-RT at least once before performing the steps below. Otherwise, macOS will block the application because it has changed.**

Open a terminal and navigate to the RTS directory within Papyrus-RT then run ```BUILDTOOLS=darwin make```. 
```
cd <INSTALL_DIR>/Papyrus-RT.app/Contents/Eclipse/plugins/org.eclipse.papyrusrt.rts_1.0.0.201810091347/umlrts
BUILDTOOLS=darwin make
```

### On Windows
Open a Cygwin terminal, and follow the instructions below
```
cd <INSTALL_DIR>/Papyrus-RT/plugins/org.eclipse.papyrusrt.rts_1.0.0.201810091347/umlrts
mkdir rts && cd rts
cmake ..
make
mv librtsd.a ../lib/linux.cygwin/librts.a
```
**Note:** to access the Windows C drive from a Cygwin terminal you have to use ```/cygdrive/c```. So if ```<INSTALL_DIR>``` is the Desktop folder, the full path will look something like:
```
/cygdrive/c/Users/kjahed/Desktop/Papyrus-RT/plugins/org.eclipse.papyrusrt.rts_1.0.0.201810091347/umlrts
```
### References
https://wiki.eclipse.org/Papyrus-RT/User/User_Guide/Building_the_RTS
