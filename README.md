# katalon-gradle-plugin-local
This is an Katalon Studio sample project to use [katalon gradle plugin](https://github.com/katalon-studio/katalon-gradle-plugin) in local

### How to use

1. Clone this project
2. Copy the `jars` folder of the this project into your project
3. Open the replace your build.gradle file with this content

```groovy
buildscript {
    dependencies{
        classpath files('jars/katalon-gradle-plugin-0.0.7.jar')
        classpath files('jars/shadow-4.0.4.jar')
    }
}

plugins {
  id 'java'
}

apply plugin: com.katalon.gradle.plugin.KatalonGradlePlugin
``` 