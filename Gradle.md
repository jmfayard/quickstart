# 🚀 QUICKSTART gradle

## 🧭 What is Gradle and who should use it ?

Gradle is a powerful build automation tool primarily used for Java, Kotlin, and Android projects. It handles tasks like compiling code, running tests, packaging artifacts, managing dependencies, and publishing.

## 👩‍💻 Who should use it ? 

**Intended audience**  
  - Java/Kotlin developers who want high flexibility in build configuration  
  - Android developers (Gradle is the official Android build system)  
  - Backend devs who value performance and task automation

- **Main competitors**  
  - Maven (convention-over-configuration, XML-based)
  - Bazel (used at Google, fast but complex)


- **Gradle key benefits**  
  - Fast incremental builds and build caching  
  - Kotlin DSL: type-safe, IDE-friendly build scripts  
  - Plugin ecosystem and extensibility  
  - Fine-grained task management and dependencies  
  - First-class support for multi-module projects

- **You may not like it if...**  
  - You prefer strict conventions and zero setup (Maven may suit you better)  
  - You dislike DSLs and prefer declarative XML  
  - You want a build system that's preconfigured and doesn't require fine-tuning


## 📚 Useful Resources
- https://docs.gradle.org/current/userguide/userguide.html
- https://start.spring.io/ (select Gradle)

## 🧰 Prerequisites

Install various versions of Java, the latest one, the lastest stable and the your project use.

Personally I install Java JVMs via IntelliJ : https://www.jetbrains.com/guide/java/tips/download-jdk/


## First step

- `gradle init`
- or **IntelliJ** → New Project → Gradle (Kotlin DSL)
- or **Spring Initializr** with Gradle & Kotlin DSL https://start.spring.io/
- or **Ktor** initializr https://start.ktor.io
- ...


## 📂 Files

```
my-project/
├── gradle/
│   ├── wrapper/
│   │   ├── gradle-wrapper.jar          
│   │   └── gradle-wrapper.properties   # Gradle version
│   └── libs.versions.toml              # 📦 Version Catalog (type-safe deps)
├── settings.gradle.kts            # Includes build-logic, enables type-safe accessors
├── gradle.properties              # JVM args, project-wide settings

# Project builds
├── build.gradle.kts               # Main build file
├── app/
│   └── build.gradle.kts           # 'app' build file
├── core/
│   └── build.gradle.kts


# ✅ Build output & cache (gitignored)
├── .gradle/
├── build/


# ✅ refreshVersions support
├── versions.properties            # 📌 Locked versions (autogenerated)
├── gradle/libs.versions.toml      # 🔁 Used alongside refreshVersions
```

## Custom Setup

What I always do
- I setup [[gradle refreshVersions]]
- I setup [[Gradle buildscan]]
- I configure `gradle.properties` following https://dev.to/jmfayard/configuring-gradle-with-gradle-properties-211k
- [[snippets/gradle common config]]  to configure the Java Version, Junit Platform, ...  

What I sometimes do
- [[local convention plugins]] 


## 🐚 Important commands

```bash
# Compile the project
$ ./gradlew build

# Run tests
$ ./gradlew test

# Run app (if Spring Boot)
$ ./gradlew bootRun
```



