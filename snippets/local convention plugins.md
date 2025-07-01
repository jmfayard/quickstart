Goal: Declarative plugins to be shared across modules
See https://docs.gradle.org/current/samples/sample_convention_plugins.html

```

# ✅ Local convention plugins
├── build-logic/                  
│   ├── build.gradle.kts
│   ├── settings.gradle.kts
│   └── my-plugin/
│       ├── build.gradle.kts
│       └── src/main/kotlin/
│           └── MyPlugin.kt
```