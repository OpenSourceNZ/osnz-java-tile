# tile-properties

A tile defines resoures and test resources.

## How to use

```xml

...

<properties>
  <!-- default -->
  <project.tile.properties.resource.delimiter>@</project.tile.properties.resource.delimiter>

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
            <tile>io.osnz.tiles:tile-properties:[1,2)</tile>
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
