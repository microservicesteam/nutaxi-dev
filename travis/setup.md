
# Setup of Travis CI

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
* Add the given project's badge to project's `README.md` file
  * Copy the badge's URL from the actual build
