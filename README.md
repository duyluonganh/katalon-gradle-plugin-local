# katalon-gradle-plugin-local
This is an Katalon Studio sample project to use [katalon gradle plugin](https://github.com/katalon-studio/katalon-gradle-plugin) in local

### How to use

1. Clone this project
2. Copy the `jars` folder of the this project into your project
3. Open and modify your build.gradle file with this content

```groovy
buildscript {
    dependencies{
        classpath files('jars/katalon-gradle-plugin-0.0.7.jar')
        classpath files('jars/shadow-6.1.0-fix-log4shell.jar')
    }
}

plugins {
  id 'java'
}

apply plugin: com.katalon.gradle.plugin.KatalonGradlePlugin
``` 

### Log4Shell concern
This project has included the [internal build](https://github.com/duyluonganh/shadow) for shadow project to resolve Log4Shell issue.