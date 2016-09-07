
# Setup of Codecov

* Update the given project's  `.travis.yml` file

```yml
after_success:
  - bash <(curl -s https://codecov.io/bash)
```

* Update the given project's  `pom.xml` file with the following plugin

```xml
 <plugin>
    <groupId>org.jacoco</groupId>
    <artifactId>jacoco-maven-plugin</artifactId>
    <version>${jacoco-maven-plugin}</version>
    <executions>
        <execution>
            <id>default-prepare-agent</id>
            <goals>
                <goal>prepare-agent</goal>
            </goals>
        </execution>
        <execution>
            <id>default-prepare-agent-integration</id>
            <goals>
                <goal>prepare-agent-integration</goal>
            </goals>
        </execution>
        <execution>
            <id>default-report</id>
            <goals>
                <goal>report</goal>
            </goals>
        </execution>
        <execution>
            <id>default-report-integration</id>
            <goals>
                <goal>report-integration</goal>
            </goals>
        </execution>
    </executions>
</plugin>
```

* Go to https://codecov.io/
* Select *microservices* organization
* Select the given project
* Add the given project's badge to project's `README.md` file
  * Copy the badge's URL from the Settings tab of the given project
