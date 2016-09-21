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

* [Setup](checkstyle/setup.md) Checkstyle for the given project

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

## Maven best practices

* Extract every dependency version into properties with the following property name: <artifactId.version>


## Git Best practices

* Use the following [.gitignore](git/.gitignore) file

#### Workflow

* Working with [nutaxi-project](https://github.com/microservicesteam/nutaxi)
  1. Nutaxi comes with submodules
  2. By default you can work (commit/push/pull) with nutaxi repository only
  3. Submodules represent a snapshot view only on the sub repositories (HEAD is detached)
  4. In order to work with submodules you need to checkout master in the appropriate submodule folder -> Head will be attached again: *git checkout master*

#### Adding submodule

* Link the new project as [submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) to our [base project](https://github.com/microservicesteam/nutaxi)
  * Refresh your repository: *git submodule update --init --recursive*
  * Use the following command: *git submodule add `URL`*
* Update the [base project](https://github.com/microservicesteam/nutaxi) manually
  * Use the following command: *git submodule update --remote*
  * Then push the changes
