Android Settings

Concept
    1. JNI (Java Native Interface)
        Java Codes <--|JNI|--> Native (C, C++, Assembly)
        Android : Java Layer <--> C, C++ Layer

Android Studio Setting Process
    Android Studio
    1. Install NDK
    2. Set Android NDK Location 
    * In My Case : Download Android NDK here (https://developer.android.com/ndk/downloads/index.html)
    3. Added javah, NDK-build, NDK-clean to [External Tools]
    * Javah Parameter : -classpath "$Classpath$" -v -jni $FileClass$
    * Javah's delimiter is blank. 
    * Previous Parameter : -classpath $Classpath$ -v -jni $FileClass$
    * Javah takes a fully qualified class name, and classpath. Class name must be with full package name.
 
JNI Process
    1. Write java code (declaire native func)
    2. Build Java Source -> Get class file
    3. Create header file from class file by Javac
    4. Write C/C++ code on the basis of header file.
    5. Create .so(Shared Object) library by compile C/C++ code.
    6. Execute android java application include with library

Device Setting
    1. Set same static ip(ethernet) with PC's ip
    2. Android Studio : abd connect [static_ip:port]
    3. Execute button -> select device