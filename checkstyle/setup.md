
# Setup of checkstyle

* Update the given project's  `build.gradle` file

	* Add the following dependency and lines

```groovy
classpath("de.undercouch:gradle-download-task:3.1.1")
```


```groovy
apply plugin: 'de.undercouch.download'
apply plugin: 'checkstyle'

task checkstyleConfigDownload(type: de.undercouch.gradle.tasks.download.Download) {
    src 'https://raw.githubusercontent.com/microservicesteam/nutaxi-dev/master/config/checkstyle/checkstyle.xml'
    dest buildDir
}

checkstyle {
    toolVersion = "7.1"
    configFile = new File(buildDir, "checkstyle.xml")
}

checkstyleMain.dependsOn checkstyleConfigDownload
checkstyleTest.dependsOn checkstyleConfigDownload
```
