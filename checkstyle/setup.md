
# Setup of checkstyle

* Update the given project's `pom.xml` file with the following plugin

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-checkstyle-plugin</artifactId>
    <version>${maven-checkstyle-plugin.version}</version>
    <executions>
        <execution>
            <id>validate</id>
            <phase>validate</phase>
            <configuration>
                <configLocation>https://raw.githubusercontent.com/microservicesteam/nutaxi-dev/master/config/checkstyle/checkstyle.xml</configLocation>
                <encoding>UTF-8</encoding>
                <consoleOutput>true</consoleOutput>
                <failsOnError>true</failsOnError>
                <linkXRef>false</linkXRef>
            </configuration>
            <goals>
                <goal>check</goal>
            </goals>
        </execution>
    </executions>
</plugin>

```
