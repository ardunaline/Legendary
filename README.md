Legendary
===========

Paper fork for the "Legends" project.
The fork is based off of the framework used in Spottedleaf's Concrete


How To (Plugin Developers)
------

* Maven Repo (for legendary-api):
```xml
<!--Coming soon!-->
```
* Artifact Information:
```xml
<dependency>
    <groupId>net.parkerMC.legendary</groupId>
    <artifactId>legendary-api</artifactId>
    <version>1.18.1-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
 ```

**Or alternatively, with Gradle:**

* Repository:
```kotlin
repositories {
    maven {
        //Coming soon!
    }
}

dependencies {
    compileOnly("net.parkermc.legendary:legendary-api:1.18.1-R0.1-SNAPSHOT")
}

java {
    toolchain.languageVersion.set(JavaLanguageVersion.of(17))
}
```

How To (Compiling Jar From Source)
------
To compile Legendary, you need JDK 17 and an internet connection.

Clone this repo, run `./gradlew applyPatches`, then `./gradlew paperclipJar` from your terminal. You can find the compiled jar in the project root's `build/libs` directory.

How To (Patches)
------
Patches are effectively just commits in either Legendary-API or Legendary-Server.
To create one, just add a commit to either repo and run `./gradlew rebuildPatches`, and a
patch will be placed in the patches folder. Modifying commits will also modify its
corresponding patch file.
