# tile-spring-boot

A tile based on `jib-maven-plugin` to build the docker image.

## How to use

```xml

...

<properties>
    <!-- plugin version -->
    <project.tiles.spring-boot-maven-plugin.version>2.6.3</project.tiles.spring-boot-maven-plugin.version>
</properties>

...

<build>
  <plugins>
    <plugin>
      <groupId>io.repaint.maven</groupId>
      <artifactId>tiles-maven-plugin</artifactId>
      <version>2.26</version>
      <extensions>true</extensions>
        <configuration>
          <filtering>false</filtering>
          <tiles>
            <tile>io.osnz.tiles:tile-spring-boot:[1,2)</tile>
          </tiles>
        </configuration>
    </plugin>
  </plugins>
</build>


```

