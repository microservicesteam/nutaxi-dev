# nutaxi-dev
Tools, IDE and other tools' configurations, guidelines, best practices for nutaxi developers

## Tools

### [Travis CI](https://travis-ci.org/)

* Add a `.travis.yml` file to the root of project (next to the your `build.gradle` file)
* Copy the basic configuration into this file

```yml
language: java
jdk:
  oraclejdk8
script:
  - ./gradlew clean build
```
* Go to https://travis-ci.org/
* Add new repository
* Select *microservices* organization
* Enable the given project

### [Codecov](https://codecov.io/)
### [VersionEye](https://www.versioneye.com/)

## Code quality

### [Checkstyle](http://checkstyle.sourceforge.net/)
### [PMD](https://pmd.github.io/)
### [FindBugs](http://findbugs.sourceforge.net/)

## Project structure

## Code formatting

TBD


## Coding guidelines

TBD

## Spring best practices

TBD

## Gradle best practices

TBD
