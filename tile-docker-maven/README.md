# tile-docker-maven

A tile based on `docker-maven-tile` to build the docker image.

## How to use

### Properties in pom.xml

```xml
<properties>
  <!-- default -->
  <docker.registry>docker.io</docker.registry>
  <docker.imageName>${project.artifactId}</docker.imageName>
  <docker.imageFullName>${docker.registry}/${docker.imageName}</docker.imageFullName>
  <docker.releaseTag>${project.version}</docker.releaseTag>
  <docker.latestTag>latestTag</docker.latestTag>

  <docker.dockerFile>${project.basedir}/Dockerfile</docker.dockerFile>
  <docker.contextDir>${project.basedir}</docker.contextDir>
  <docker.filter>@</docker.filter>

  <docker.auth.username>changeme</docker.auth.username>
  <docker.auth.password>changeme</docker.auth.password>
</properties>
```

### Plugin in pom.xml

```xml
  <build>
    <plugins>
      ...
      <plugin>
        <groupId>io.repaint.maven</groupId>
        <artifactId>tiles-maven-plugin</artifactId>
        <version>2.16</version>
        <extensions>true</extensions>
        <configuration>
          <tiles>
            <tile>io.osnz.tiles:tile-docker-maven:[1,2)</tile>
          </tiles>
        </configuration>
      </plugin>
    </plugins>
  </build>
```

## Execution with profiles

### Build image

```bash
mvn clean install
```

### Build image and push image to registry without authentication


```bash

mvn clean install -Pdocker-push

```

### Build image and push to registry with authentication

```bash

mvn clean install -Pdocker-auth-push -Ddocker.auth.username=changeme -Ddocker.auth.password=changeme

```
