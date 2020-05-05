# tile-helm

A tile based on `maven-resources-plugin` to generate helm resources.

## How to use

```xml

...

<properties>
  <!-- default -->
  <project.tile.helm.resource.delimiter>@</project.tile.helm.resource.delimiter>
  <project.tile.helm.source>${project.basedir}/cloudbuild/helm</project.tile.helm.source>
  <project.tile.helm.output>${project.build.directory}/cloudbuild/helm</project.tile.helm.output>
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
            <tile>io.osnz.tiles:tile-helm:[1,2)</tile>
          </tiles>
        </configuration>
        <dependencies>
          <dependency>
            <groupId>com.gkatzioura.maven.cloud</groupId>
            <artifactId>google-storage-wagon</artifactId>
            <version>1.7</version>
          </dependency>
        </dependencies>
    </plugin>
  </plugins>
</build>


```
