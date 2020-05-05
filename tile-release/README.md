# OSS Release Tile

```xml
    <build>
        <plugins>
            <plugin>
                <groupId>io.repaint.maven</groupId>
                <artifactId>tiles-maven-plugin</artifactId>
                <version>2.12</version>
                <extensions>true</extensions>
                <configuration>
                    <tiles>
                        <tile>io.osnz.tiles:release-tile:[1.0,)</tile>
                    </tiles>
                </configuration>
            </plugin>
        </plugins>
    </build>
```