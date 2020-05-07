# Groovy Compiler Tile under test scope

Groovy Tile for all groovy-based artifacts under test scope

## How to use

### Properties in pom.xml

```xml
<properties>
  <!-- default -->
  <project.tiles.gmavenplus-plugin.version>1.9.0</project.tiles.gmavenplus-plugin.version>
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
            <tile>io.osnz.tiles:tile-groovy-test:[1,2)</tile>
          </tiles>
        </configuration>
      </plugin>
    </plugins>
  </build>
```
