
# Setup of FindBugs

* Update the given project's  `build.gradle` file

```groovy
apply plugin: 'findbugs'

findbugs {
	toolVersion = "5.5.1"
}

```