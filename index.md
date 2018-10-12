## Making Modeling Cool Again!

This repository contains all the tools and files needed to get your hands dirty at the Making Modeling Cool Again tutorial. The tutorial will cover the use of **Papyrus-RT** to 
- Connect and manipulate 3D simulations built using the Unity3D game engine.
- Integrate Papyrus-RT models with the Internet-of-Things using the **MQTT** protocol
- Augmenting Papyrus-RT models with complex cloud services using MQTT and **Node-RED**

### Prerequisite 
- Papyrus-RT requires [Java 8 (64-bit)](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) to operate correctly. It will not work with newer versions of Java.
- Building the generated code requires ```g++``` and ```make```:
  - On Windows, install [Cygwin](https://www.cygwin.com/) with the ```gcc-g++``` and ```make``` packages.
  - On macOS, install the Xcode Command Line Tools using the command ```xcode-select --install```
  - On Linux, you probably know what you need to do
  
### Download Papyrus-RT
The tutorial will use a special build of Papyrus-RT. Download and extract the appropriate version for your system:
- [Windows](https://github.com/kjahed/Models18-MMCA/releases/download/1.0/papyrusrt-windows.zip)
- [macOS](https://github.com/kjahed/Models18-MMCA/releases/download/1.0/papyrusrt-macos.zip)
- [Linux](https://github.com/kjahed/Models18-MMCA/releases/download/1.0/papyrusrt-linux.zip)

### Grab the Simulation
The pre-build Unity-3D simulation for the Safe model that will be used throughout the tutorial can be downloaded from here:
- [Windows](https://github.com/kjahed/Models18-MMCA/releases/download/1.0/safesim-windows.zip)
- [macOS](https://github.com/kjahed/Models18-MMCA/releases/download/1.0/safesim-macos.zip)
- [Linux](https://github.com/kjahed/Models18-MMCA/releases/download/1.0/safesim-linux.zip)

### Grab the examples
Download the zip file from [here](https://github.com/kjahed/Models18-MMCA/releases/download/1.0/examples.zip)

### CloudMQTT
We will use MQTT to connect the models to the Internet-of-Things. For that, you'll need to run an MQTT broker. [CloudMQTT](https://www.cloudmqtt.com) offers a hosted MQTT broker for free. Register for an account [here](https://customer.cloudmqtt.com/instance/create?plan=cat)

### Node-RED
We will Node-RED to integrate Papyrus-RT models with cloud services and APIs. IBM Bluemix offers a (limited) Node-RED instance for free. Register for an IBM Cloud account [here](https://console.bluemix.net/registration/). We will show how to setup the Node-RED instance during the tutorial.

# That's it! You're ready.
