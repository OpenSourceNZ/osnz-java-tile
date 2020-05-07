# tile-docker-jib

A tile based on `jib-maven-plugin` to build the docker image.

## How to use

```xml

...

<properties>
    <docker.mainClass>io.osnz.Application</.docker.mainClass>
    <docker.appProperties>-P/etc/app/app.properties</docker.appProperties>
    <docker.secretProperties>-P/etc/app/secret.properties</docker.secretProperties>
    <docker.argument1>-DdevMode=false</docker.argument1>
    <docker.argument2>-Denv=PROD</docker.argument2>

    <!-- project settings -->
    <docker.baseImage>openjdk:11-jre-slim-stretch</docker.baseImage>
    <docker.registry>docker.io</docker.registry>
    <docker.imageName>${project.artifactId}</docker.imageName>
    <docker.fullName>${docker.registry}/${docker.imageName}</docker.fullName>
    <docker.currentTag>${project.version}</docker.currentTag>
    <docker.latestTag>latest</docker.latestTag>
    <docker.port>8080</docker.port>

    <docker.auth.username>changeme</docker.auth.username>
    <docker.auth.password>changeme</docker.auth.password>

    <!-- maven tile plugin version -->
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
            <tile>io.osnz.tiles:tile-jib-docker-bathe:[1,2)</tile>
          </tiles>
        </configuration>
    </plugin>
  </plugins>
</build>


```
