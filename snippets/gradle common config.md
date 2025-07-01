## Configure the build scan

```kotlin
// ./settings.gradle.kts
plugins {
    id("com.gradle.enterprise") version "VERSION"
}

gradleEnterprise {
    buildScan {
        termsOfServiceUrl = "https://gradle.com/terms-of-service"
        termsOfServiceAgree = "yes"
        publishAlways()
    }
}
```

2. run it
`./gradlew build --scan`

3. validate your email the first time
4. see the build scan URL

## Setup Java version

```
java {
    toolchain {
        languageVersion.set(JavaLanguageVersion.of(21))
    }
}
```

## Use Junit
```kotlin
tasks.test {
    useJUnitPlatform()
}
```
