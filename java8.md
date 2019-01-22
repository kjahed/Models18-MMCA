# Java 8
Papyrus-RT requires [Java 8 (64-bit)](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) to operate correctly. It will not work with newer versions of Java. After installing Java 8, if you happen to have another version of Java, Papyrus-RT might pick up the wrong one. If Papyrus-RT crashes upon startup you need to update the Papyrus-RT  configuration file to include the path to Java 8.

## Step 1
Figure out the path to the Java 8's ```bin``` directory on your system:

#### On macOS
Open a terminal and run the command ```/usr/libexec/java_home -v1.8```
The output should look like 
```
/Library/Java/JavaVirtualMachines/jdk1.8.0_191.jdk/Contents/Home
```
The full path would then be ```/Library/Java/JavaVirtualMachines/jdk1.8.0_191.jdk/Contents/Home/bin```

#### On Linux (Ubuntu)
Open a terminal and run the command ```update-alternatives --list java```
It will give you the paths to all the Java's installed on your system, e.g.
```
/usr/bin/gij-5
/usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java
```
Find the one that contains ```8``` or ```1.8```. The full path will then look like ```/usr/lib/jvm/java-8-openjdk-amd64/jre/bin```

#### On Windows
Java is typically installed to ```C:\Program Files\Java```. If you have multiple versions of Java installed, you will have multiple folders whithin that directory. Find the folder that contains ```1.8``` in its name, e.g. ```jdk1.8.0_191```. The full path will then look like ```C:\Program Files\Java\jdk1.8.0_191\bin```

## Step 2
Find the ```papyrusrt.ini``` file. On Linux and Windows, the file can be found whithin the main Papyrus-RT directory. On macOS, right click on Papyrus-RT and choose "Show Package Contents" then navigate to ```Contents/Eclipse```.

## Step 3
Edit the ```papyrusrt.ini``` file and append the following to the end. Replace ```<java_8_path>``` with the path you obtained in [Step 1](#step-1).
```
-vm <java_8_path>
```
e.g.
```
-vm /Library/Java/JavaVirtualMachines/jdk1.8.0_191.jdk/Contents/Home/bin
```
