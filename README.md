# Voqal Android SDK — Maven distribution

Public, binary-only distribution for the **Voqal Android SDK**. This repository hosts the
compiled `.aar` and its dependency metadata only — the SDK source is private.

It is served directly over `raw.githubusercontent.com` as a Maven repository, so there is
nothing to build and no account, token, or subscription required.

## Latest version

`ai.voqal:voqal-sdk:1.0.2`

## Install

**1. Add the repository** in `settings.gradle.kts` (Kotlin DSL):

```kotlin
dependencyResolutionManagement {
    repositories {
        google()
        mavenCentral()
        maven { url = uri("https://raw.githubusercontent.com/VoqalAI/voqal-android-maven/main") }
    }
}
```

<details>
<summary>Groovy DSL (<code>settings.gradle</code>)</summary>

```groovy
dependencyResolutionManagement {
    repositories {
        google()
        mavenCentral()
        maven { url 'https://raw.githubusercontent.com/VoqalAI/voqal-android-maven/main' }
    }
}
```
</details>

**2. Add the dependency** in your app module's `build.gradle.kts`:

```kotlin
dependencies {
    implementation("ai.voqal:voqal-sdk:1.0.2")
}
```

Transitive dependencies (Jetpack Compose, AndroidX, Kotlin stdlib) resolve automatically
from the published POM.

## Requirements

- `minSdk` 28+, `compileSdk` 35
- JDK 17
- Jetpack Compose

## Usage

See the full integration guide at **https://voqal.ai/docs** (Android).
