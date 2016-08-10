# nutaxi-dev
Tools, IDE and other tools' configurations, guidelines, best practices for nutaxi developers

## Tools

### [Travis CI](https://travis-ci.org/)

* [Setup](travis/setup.md) Travis CI for the given project

### [Codecov](https://codecov.io/)


* [Setup](codecov/setup.md) Codecov for the given project

### [VersionEye](https://www.versioneye.com/)

## Code quality

### [Checkstyle](http://checkstyle.sourceforge.net/)
### [PMD](https://pmd.github.io/)

* [Setup](pmd/setup.md) PMD for the given project

### [FindBugs](http://findbugs.sourceforge.net/)

* [Setup](findbugs/setup.md) FindBugs for the given project

## Project structure

* TBD

## Code formatting

For `Java` based projects use the following [formatting profile](config/formatting/nutaxi-formatting-profile.xml)


## Coding guidelines

* TBD

## Spring best practices

* TBD

## Gradle best practices

* TBD

## Git Best practices

* Use the following [.gitignore](git/.gitignore) file
* Link the new project as [submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) to our [base project](https://github.com/microservicesteam/nutaxi)
  * Use the following command: *git submodule add `URL`*
* Update the [base project](https://github.com/microservicesteam/nutaxi) manually
  * Use the following command: *git submodule update --remote*
  * Then push the changes
