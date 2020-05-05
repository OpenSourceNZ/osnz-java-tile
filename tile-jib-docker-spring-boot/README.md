# tile-docker-jib

A tile based on `jib-maven-plugin` to build the docker image.

## How to use

```xml

...

<properties>
  <!-- default -->
  <docker.registry>docker.io</docker.registry>
  <docker.image.from>openjdk:11.0.4-jre-slim</docker.image.from>
  <docker.image.name>${docker.registry}/${project.artifactId}</docker.image.name>
  <docker.image.tag>${project.version}</docker.image.tag>
  <docker.image.tag2>latest</docker.image.tag2>
  <docker.image.port>8080</docker.image.port>
  <docker.auth.username>changeme</docker.auth.username>
  <docker.auth.password>changeme</docker.auth.password>
  <app.arguments>-DdevMode=false</app.arguments>
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

