# Installation_Java_8
How to Install Oracle Java 8 (JDK 8u25) on CentOS/RHEL 6/5 and Fedora

Step 1: Download JAVA Archive 

For 64 bits
# cd /opt/
# wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u25-b17/jdk-8u25-linux-x64.tar.gz"
# tar xzf jdk-8u25-linux-x64.tar.gz

For 32 bits
# cd /opt/
# wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u25-b17/jdk-8u25-linux-i586.tar.gz"
# tar jdk-8u25-linux-i586.tar.gz

Step 2: Install JAVA using Alternatives
# cd /opt/jdk1.8.0_25/
# alternatives --install /usr/bin/java java /opt/jdk1.8.0_25/bin/java 2
# alternatives --config java
There are 3 programs which provide 'java'.

  Selection    Command
-----------------------------------------------
*  1           /opt/jdk1.8.0/bin/java
 + 2           /opt/jdk1.7.0_55/bin/java
   3           /opt/jdk1.8.0_25/bin/java

Enter to keep the current selection[+], or type selection number: 3
# alternatives --install /usr/bin/jar jar /opt/jdk1.8.0_25/bin/jar 2
# alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_25/bin/javac 2
# alternatives --set jar /opt/jdk1.8.0_25/bin/jar
# alternatives --set javac /opt/jdk1.8.0_25/bin/javac 

Step 3: Check Version of JAVA .
# java -version 
java version "1.8.0_25"
Java(TM) SE Runtime Environment (build 1.8.0_25-b17)
Java HotSpot(TM) 64-Bit Server VM (build 25.25-b02, mixed mode)

Step 4: Setup Environment Variables 
Setup JAVA_HOME Variable
# export JAVA_HOME=/opt/jdk1.8.0_25
Setup JRE_HOME Variable
# export JRE_HOME=/opt/jdk1.8.0_25/jre
Setup PATH Variable
# export PATH=$PATH:/opt/jdk1.8.0_25/bin:/opt/jdk1.8.0_25/jre/bin

