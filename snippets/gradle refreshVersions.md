**refreshVersions** simplifies Gradle dependency updates by:

- Automatically migrating your build to use version catalogs,
- Checking for updates,
- Annotating the TOML/properties file with what's new,
- And cleaning up stale comments when done.

## URLs

https://splitties.github.io/refreshVersions
## Setup

### Plugin Installation

In your `settings.gradle.kts`:

```kotlin
// MUST be at the top of the file
pluginManagement {
    plugins {
        id("de.fayard.refreshVersions") version "VERSION"
    }
}

plugins {
    id("de.fayard.refreshVersions")
}

// See https://splitties.github.io/refreshVersions/setup/#configure-the-plugin
refreshVersion {
   // ....
}
```

### Migrate

```
./gradlew refreshVersionsMigrate --mode=VersionCatalogAndVersionProperties
```

### Updates

```
# Step 1
./gradle refreshVersions

# Step 2 : 
# Edit "versions.properties" or "libs.versions.toml"
```

