# tile-node

This tile plugin is used to compile node-based artifact.

## How to use it

```json
{
  "scripts": {
    "test": "",
    "build": "",
    "eslint": "",
    "sonar": ""
  }
}

```

```xml
  <build>
    <plugins>
      ...
      <plugin>
        <groupId>io.repaint.maven</groupId>
        <artifactId>tiles-maven-plugin</artifactId>
        <version>2.15</version>
        <extensions>true</extensions>
        <configuration>
          <tiles>
            <tile>io.osnz.tiles:tile-node:[1.1,2)</tile>
          </tiles>
        </configuration>
      </plugin>
    </plugins>
  </build>
```

### Enable sonar scan

```bash

mvn clean verify -Psonar

```

### Enable eslint

```bash

mvn clean verify -Peslint

```
