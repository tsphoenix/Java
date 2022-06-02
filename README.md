# Java

https://en.wikipedia.org/wiki/Java_version_history

https://adoptopenjdk.net/

**Documentation (LTS):**

https://docs.oracle.com/en/java/

https://docs.oracle.com/javase/8/

https://docs.oracle.com/javase/8/docs/

https://docs.oracle.com/en/java/javase/11/


**Windows Environmental Variables**
Access to Environmental Variables is often blocked in GUI on corpotate Windows Laptops.

 

We may list and edit these in powershell and cmd

 

An environment variable (name and value pair) is a variable whose value is set outside the program, through functionality built into the operating system.

 

There are two types of installations in windows:

Privileged installations(requiring administrative rights aka admin account):

in Program Files:

 

Progra~1 = 'Program Files'

Progra~2 = 'Program Files(x86)'

 

User profile installations - anything that is in user profile

C:\Users\%USERPROFILE%

%USERPROFILE%

%USERPROFILE%\AppData\Local\Programs




Listing Environmental Variables:

 

cmd

 

set

 

powershell

 

dir env:

 

System Variables

 

reg query "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Environment"




User Variables

 

reg query HKEY_CURRENT_USER\Environment

 

JAVA_HOME : C:\Program Files\Java\jdk1.8.0_331

JDK_HOME : %JAVA_HOME%

JRE_HOME : %JAVA_HOME%\jre

CLASSPATH : .;%JAVA_HOME%\lib;%JAVA_HOME%\jre\lib

PATH : your-unique-entries;%JAVA_HOME%\bin

 

Set User Variables for JAVA (legacy jdk1.8.0_331 example)

 

setx JAVA_HOME "C:\Program Files\Java\jdk1.8.0_331"

setx JDK_HOME "%JAVA_HOME%"

setx JRE_HOME %JAVA_HOME%\jre

 

setx PATH "%PATH%;%JAVA_HOME%\bin";

 

Set System Variables for JAVA (legacy jdk1.8.0_331 example)

 

setx -m JAVA_HOME "C:\Program Files\Java\jdk1.8.0_331"

setx -m PATH "%PATH%;%JAVA_HOME%\bin";
