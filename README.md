# myApacheSparkScala
Learning Snippets about Apache Spark and Scala


## Installing Apache Spark and Scala
- Windows:
  1. Install a JDK (Java Development Kit) from http://www.oracle.com/technetwork/java/javase/downloads/index.html . Keep track of where you installed the JDK; you’ll need that later. DO NOT INSTALL JAVA 9, 10, or 11 – INSTALL JAVA 8. Spark is not compatible with Java 9 or greater. And BE SURE TO INSTALL JAVA TO A PATH WITH NO SPACES IN IT. Don’t accept the default path that goes into “Program Files” on Windows, as that has a space.
  1. Download a pre-built version of Apache Spark 3.0.0 or 2.4.4 depending on which version of the course you’re taking  from https://spark.apache.org/downloads.html
  1. If necessary, download and install WinRAR so you can extract the .tgz file you downloaded. http://www.rarlab.com/download.htm
  1. Extract the Spark archive, and copy its contents into C:\spark after creating that directory. You should end up with directories like c:\spark\bin, c:\spark\conf, etc.
  1. Download winutils.exe from https://sundog–s3.amazonaws.com/winutils.exe and move it into a C:\winutils\bin folder that you’ve created. (note, this is a 64-bit application. If you are on a 32-bit version of Windows, you’ll need to search for a 32-bit build of winutils.exe for Hadoop.)
  1. Create a c:\tmp\hive directory, and cd into c:\winutils\bin, and run winutils.exe chmod 777 c:\tmp\hive
  1. Open the the c:\spark\conf folder, and make sure “File Name Extensions” is checked in the “view” tab of Windows Explorer. Rename the log4j.properties.template file to log4j.properties. Edit this file (using Wordpad or something similar) and change the error level from INFO to ERROR for log4j.rootCategory
  1. Right-click your Windows menu, select Control Panel, System and Security, and then System. Click on “Advanced System Settings” and then the “Environment Variables” button.
  1. Add the following new USER variables mentioned below
  1. Close the environment variable screen and the control panels.
  1. Install the latest Scala IDE from http://scala-ide.org/download/sdk.html
  1. Test it out!
  1. Open up a Windows command prompt in administrator mode.
  1. Enter cd c:\spark and then dir to get a directory listing.
  1. Look for a text file we can play with, like README.md or CHANGES.txt
  1. Enter spark-shell
  1. At this point you should have a scala> prompt. If not, double check the steps above.
  1. Enter val rdd = sc.textFile(“README.md”) (or whatever text file you’ve found) Enter rdd.count()
  1. You should get a count of the number of lines in that file! Congratulations, you just ran your first Spark program!
  1. Hit control-D to exit the spark shell, and close the console window
  1. You’ve got everything set up! Hooray!

    ```
    SPARK_HOME c:\spark
    JAVA_HOME (the path you installed the JDK to in step 1, for example C:\ProgramFiles\Java\jdk1.8.0_101)
    HADOOP_HOME c:\winutils
    Add the following paths to your PATH user variable:
    %SPARK_HOME%\bin
    %JAVA_HOME%\bin
    ```


- MacOS
  + Step 1: Install Spark
  + Step 2: Install the Scala IDE
  + Step 3: Test it out!

__Step 1: Install Spark__
Method A: By Hand
The best setup instructions for Spark on MacOS are at the following link:

https://medium.com/luckspark/installing-spark-2-3-0-on-macos-high-sierra-276a127b8b85

Spark 2.3.0 is no longer available, but the same process should work with 2.4.4 or 3.0.0.

Method B: Using Homebrew
An alternative on MacOS is using a tool called Homebrew to install Java, Scala, and Spark – but first you need to install Homebrew itself.

Step by step instructions are at https://www.tutorialkart.com/apache-spark/how-to-install-spark-on-mac-os/

__Step 2: Install the Scala IDE__
Install the Scala IDE from http://scala-org/download/sdk.html

__Step 3: Test it out!__
cd to the directory apache-spark was installed to and then ls to get a directory listing.
Look for a text file we can play with, like README.md or CHANGES.txt
Enter spark-shell
At this point you should have a scala> prompt. If not, double check the steps above.
Enter val rdd = sc.textFile(“README.md”) (or whatever text file you’ve found) Enter rdd.count()
You should get a count of the number of lines in that file! Congratulations, you just ran your first Spark program!
Hit control-D to exit the spark shell, and close the console window
You’ve got everything set up! Hooray!

- Linux
1. Install Java 8, Scala, and Spark according to the particulars of your specific OS. A good starting point is http://www.tutorialspoint.com/apache_spark/apache_spark_installation.htm (be sure to install Spark 3.0.0 or 2.4.4 depending on which version of the course you’re taking)
1. Install the Scala IDE from http://scala–org/download/sdk.html
1. Test it out!
1. cd to the directory apache-spark was installed to and then ls to get a directory listing.
1. Look for a text file we can play with, like README.md or CHANGES.txt
1. Enter spark-shell
1. At this point you should have a scala> prompt. If not, double check the steps above.
1. Enter val rdd = sc.textFile(“README.md”) (or whatever text file you’ve found) Enter rdd.count()
1. You should get a count of the number of lines in that file! Congratulations, you just ran your first Spark program!
1. Hit control-D to exit the spark shell, and close the console window
1. You’ve got everything set up! Hooray!

