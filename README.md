## Maven_setup
Setup Maven on Linux Server ( CentOS 9 )



Ensure an internet connection is available.
```
ping google.com -c 5
```


Install Java 11 OpenJDK development package
```
yum install java-11-openjdk-devel -y
```

Check Java version
```
java --version
```


Download Maven from the official Apache Maven website
```
https://maven.apache.org/download.cgi
```


Use wget to download the specified version of Apache Maven
```
wget https://dlcdn.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz
```

Extract the downloaded file
```
tar -zxpvf <FileName>
```


Move the downloaded Maven archive to the /opt directory
```
mv /opt/<FileName>    /opt/maven
```


Open the .bash_profile file for editing
```
vim .bash_profile
```


Set the JAVA_HOME environment variable to the installed Java 11 OpenJDK path
```
JAVA_HOME=/usr/lib/jvm/java-11-openjdk-11.0.21.0.9-1.el7_9.x86_64
```


Set the MVN_HOME variable to the Maven installation directory
```
MVN_HOME=/opt/maven
```

Set the MVN variable to the Maven binary directory
```
MVN=/opt/maven/bin
```

Add Java and Maven paths to the system PATH variable
```
PATH=$PATH:$HOME/bin:$JAVA_HOME:$MVN_HOME:$MVN
```

Check Java version
```
mvn --version
```
