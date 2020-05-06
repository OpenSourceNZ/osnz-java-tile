# tile-node

This tile plugin is used to compile node-based artifact.

## How to use it

### Scripts in package.json

```json
{
  "scripts": {
    "test": "",
    "build": "",
    "eslint": "",
    "sonar": "",
    "report": "",
  }
}
```

### Properties in pom.xml

```xml
  <sonar.projectKey>${project.artifactId}</sonar.projectKey>
  <sonar.projectName>${project.name}</sonar.projectName>
  <sonar.organization>opensourcenz</sonar.organization>
  <sonar.host>https://sonarcloud.io</sonar.host>
  <sonar.branchName>master</sonar.branchName>
  <sonar.token></sonar.token>
  <sonar.password></sonar.password>
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
            <tile>io.osnz.tiles:tile-node-exec:[1.1,2)</tile>
          </tiles>
        </configuration>
      </plugin>
    </plugins>
  </build>
```

## Execution with profiles

```bash

mvn clean verify -Pnode-sonar,node-eslint,node-report

```
