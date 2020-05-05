# tile-docker-jib

A tile based on `jib-maven-plugin` to build the docker image.

## How to use

```xml

...

<properties>
  <!-- default -->
  <docker.image.from>openjdk:11.0.3-jdk-slim-stretch</docker.image.from.image>
  <docker.image.to.name>kdeng/${project.artifactId}</docker.image.to.name>
  <docker.image.to.tag>${project.version}</docker.image.to.tag>
  <docker.image.port>8080</docker.image.port>
</properties>

...

<build>
  <plugins>
    <plugin>
      <groupId>io.repaint.maven</groupId>
      <artifactId>tiles-maven-plugin</artifactId>
      <version>2.15</version>
      <extensions>true</extensions>
        <configuration>
          <filtering>false</filtering>
          <tiles>
            <tile>io.osnz.tiles:tile-docker-jib:[1,2)</tile>
          </tiles>
        </configuration>
    </plugin>
  </plugins>
</build>


```

