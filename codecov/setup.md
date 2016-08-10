
# Setup of Codecov

* Update the given project's  `.travis.yml`

```yml
after_success:
  - bash <(curl -s https://codecov.io/bash)
```

* Update the given project's  `build.gradle`

```groovy
apply plugin: 'jacoco'

jacoco {
    toolVersion = "0.7.7.201606060606"
}

jacocoTestReport {
    reports {
        xml.enabled = true
        html.enabled = true
    }
}

check.dependsOn jacocoTestReport
```

* Go to https://codecov.io/
* Select *microservices* organization
* Select the given project
* Add the badge to your `README.md` file
** Copy the badge's URL from the Settings tab of the given project