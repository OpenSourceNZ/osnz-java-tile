# tile-docker-jib

A tile based on `jib-maven-plugin` to build the docker image.

## How to use

```xml

...

<properties>
    <!-- project settings -->
    <docker.baseImage>openjdk:11-jre-slim-stretch</docker.baseImage>
    <docker.registry>docker.io</docker.registry>
    <docker.imageName>${project.artifactId}</docker.imageName>
    <docker.fullName>${docker.registry}/${docker.imageName}</docker.fullName>
    <docker.releaseTag>${project.version}</docker.releaseTag>
    <docker.latestTag>latest</docker.latestTag>
    <docker.port>8080</docker.port>
    <docker.argument1>-Dspring.devtools.add-properties=false</docker.argument1>
    <docker.argument2>-Dspring.jmx.enabled=false</docker.argument2>
    <docker.argument3>-DdevMode=false</docker.argument3>
    <docker.argument4>-Denv=PROD</docker.argument4>
    <docker.jvmFlag1>-noverify</docker.jvmFlag1>
    <docker.jvmFlag2>--add-exports=java.base/jdk.internal.misc=ALL-UNNAMED</docker.jvmFlag2>
    <docker.jvmFlag3>--add-opens=java.base/java.nio=ALL-UNNAMED</docker.jvmFlag3>

    <docker.auth.username>changeme</docker.auth.username>
    <docker.auth.password>changeme</docker.auth.password>

    <!-- plugin version -->
    <project.tiles.spring-boot-maven-plugin.version>2.2.6.RELEASE</project.tiles.spring-boot-maven-plugin.version>
    <project.tiles.jib-maven-plugin.version>2.2.0</project.tiles.jib-maven-plugin.version>
</properties>

...

<build>
  <plugins>
    <plugin>
      <groupId>io.repaint.maven</groupId>
      <artifactId>tiles-maven-plugin</artifactId>
      <version>2.16</version>
      <extensions>true</extensions>
        <configuration>
          <filtering>false</filtering>
          <tiles>
            <tile>io.osnz.tiles:tile-jib-docker-spring-boot:[1,2)</tile>
          </tiles>
        </configuration>
    </plugin>
  </plugins>
</build>


```

