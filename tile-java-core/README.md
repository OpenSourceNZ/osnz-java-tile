# Java Tile

Java Tile for all Java-based artifacts.



```xml
<properties>
  <project.tile.maven-resources-plugin.version>3.1.0</project.tile.maven-resources-plugin.version>
  <maven-tile.tile-helm.helm.source>${project.basedir}/src/main/resources/helm</maven-tile.tile-helm.helm.source>
  <maven-tile.tile-helm.helm.output>${project.build.directory}/helm</maven-tile.tile-helm.helm.output>
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
          <tile>io.osnz.tiles:tile-helm:[1,2)</tile>
        </tiles>
      </configuration>
    </plugin>
  </plugins>
</build>
```
