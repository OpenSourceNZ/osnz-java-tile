# docker-maven-tile

A tile based on `docker-maven-tile` to build the docker image.

## How to use

```xml

...

<properties>
  <!-- default -->
  <docker.auth.username>changeme</docker.auth.username>
  <docker.auth.password>changeme</docker.auth.password>
  <docker.registry>docker.io/kdeng</docker.registry>
  <docker.imageName>${project.artifactId}</docker.imageName>
  <docker.imageFullName>${docker.registry}/${docker.imageName}</docker.imageFullName>
  <docker.imageTag>${project.version}</docker.imageTag>
  <docker.dockerFile>${project.basedir}/Dockerfile</docker.dockerFile>
  <docker.contextDir>${project.basedir}</docker.contextDir>
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
            <tile>io.osnz.tiles:maven-docker-tile:[1,2)</tile>
          </tiles>
        </configuration>
    </plugin>
  </plugins>
</build>


```

