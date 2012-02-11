Openfire open-archive plugin
============================

This plugin, originally created by [Stefan Reuter](https://github.com/srt/) is available at:  https://github.com/srt/openarchive

This is my hack ...

To get it going...
------------------

To generate the OpenArchive SNAPSHOT jar, the following were performed in sequence:

1.  Obtain https://github.com/sdolgy/maven-openfire-plugin OR https://github.com/srt/maven-openfire-plugin and run:  maven install
2.  Obtain the openfire.jar from Openfire, and the dwr-2.0.5.jar, and install the files into the local maven repository:

     mvn install:install-file -Dfile=contrib\dwr-2.0.5.jar -DgroupId=org.directwebremoting -DartifactId=dwr -Dversion=2.0.5 -Dpackaging=jar
     mvn install:install-file -Dfile=contrib\openfire.jar -DgroupId=org.igniterealtime.openfire -DartifactId=openfire -Dversion=3.7.1 -Dpackaging=jar
     
3.  Update the pom.xml to reflect the updated Openfire version (changed to 3.7.1)
4.  maven install