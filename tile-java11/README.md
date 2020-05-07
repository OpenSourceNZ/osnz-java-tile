# Java11 Tile

Java11 Tile for all Java-based artifacts.



```xml
  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    <sonar.language>java</sonar.language>
    <java.version>11</java.version>

    <project.tiles.maven-source-plugin.version>3.2.1</project.tiles.maven-source-plugin.version>
    <project.tiles.maven-compiler-plugin.version>3.8.1</project.tiles.maven-compiler-plugin.version>
    <project.tiles.maven-compiler-plugin.compile.source>${java.version}</project.tiles.maven-compiler-plugin.compile.source>
    <project.tiles.maven-compiler-plugin.compile.target>${java.version}</project.tiles.maven-compiler-plugin.compile.target>
    <project.tiles.maven-compiler-plugin.compile.debug>false</project.tiles.maven-compiler-plugin.compile.debug>
    <project.tiles.maven-compiler-plugin.compile.optimize>true</project.tiles.maven-compiler-plugin.compile.optimize>

    <project.tiles.maven-compiler-plugin.compile.release>${java.version}</project.tiles.maven-compiler-plugin.compile.release>
    <project.tiles.maven-compiler-plugin.compile.executable>javac11</project.tiles.maven-compiler-plugin.compile.executable>
    <project.tiles.maven-compiler-plugin.compile.useIncrementalCompilation>false</project.tiles.maven-compiler-plugin.compile.useIncrementalCompilation>

    <project.tiles.maven-surefire-plugin.version>3.0.0-M4</project.tiles.maven-surefire-plugin.version>
    <project.tiles.maven-surefire-plugin.use-system-classloader>true</project.tiles.maven-surefire-plugin.use-system-classloader>
    <project.tiles.maven-surefire-plugin.useManifestOnlyJar>false</project.tiles.maven-surefire-plugin.useManifestOnlyJar>
    <project.tiles.maven-surefire-plugin.failIfNoTests>false</project.tiles.maven-surefire-plugin.failIfNoTests>

    <project.tiles.modernizer-maven-plugin.version>2.1.0</project.tiles.modernizer-maven-plugin.version>

    <project.tiles.maven-javadoc-plugin.version>3.2.0</project.tiles.maven-javadoc-plugin.version>
    <project.tiles.jacoco-maven-plugin.version>0.8.5</project.tiles.jacoco-maven-plugin.version>
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
