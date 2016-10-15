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


## Git

* Use the following [.gitignore](git/.gitignore) file

#### Guide for using Github

* `master` is always a protected branch
* no direct commits are allowed to master
* every change should go through a pull request
* accepted pull request always squashed and merged(use the button on the UI)
 * `git fetch`
 * `git rebase -i origin/master`
 * change the `pick`s to `squash`s from the second commit from the top(the first one is the base commit)
 * the final commit message is the name of the pull request
 	* [MS-{Taiga ticket number}] {Commit message}

##### Acceptance criteria of an approved Pull Request

* at least one approved code review by the team
* green CI builds
* optional: codacy, codecov, other reviews from team members

##### Code review process
* use the start review feature instead of single comments

#### Submodule workflow

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
