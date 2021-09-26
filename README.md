# flink-java-example-app-gradle

A Flink word count example application in Java with Gradle build. You can use this as the start point for your flink java application.

### Add new dependency

Add new dependency like following in `dependencies` section, this dependency will be included
in the final uber/fat jar.
```
flinkShadowJar "org.apache.flink:flink-connector-kafka_${scalaBinaryVersion}:${flinkVersion}"
```

### Build 

On Windows
```
 gradlew.bat clean build
```

On Linux/MacOS
```
 ./gradlew clean build
```

The final uber/fat jar is in `build/libs` directory, something like `build/libs/flink-java-example-app-gradle-0.1-all.jar`.

### Reference

[Flink Application Gradle Quick start](https://nightlies.apache.org/flink/flink-docs-release-1.13/docs/dev/datastream/project-configuration/#gradle)

[Gradle Shadow Plugin User Guide](https://imperceptiblethoughts.com/shadow/introduction/)

The example WordCount source code is from Apache Flink Project.