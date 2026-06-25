# kawa-runtime

Prebuilt [Kawa](https://www.gnu.org/software/kawa/) runtime jar for use as a
Maven dependency.  Served as a raw Maven repository via GitHub.

## Coordinates

```gradle
repositories {
    maven {
        name = "Kawa Runtime"
        url = uri("https://raw.githubusercontent.com/Momo-Softworks/kawa-runtime/main/")
        metadataSources { artifact() }
    }
}

dependencies {
    implementation("com.momosoftworks.kawa:kawa-runtime:3.1.1")
}
```

## Version

| Version | Kawa | Source |
|---------|------|--------|
| 3.1.1   | 3.1.1 | Built by GNU Guix |

## Updating

1. Build or obtain the new `kawa.jar`.
2. Place it at `com/momosoftworks/kawa/kawa-runtime/<version>/kawa-runtime-<version>.jar`.
3. Add a matching `.pom` file.
4. Commit and push to `main`.
