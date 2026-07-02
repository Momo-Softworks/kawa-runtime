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
    implementation("com.momosoftworks.kawa:kawa-runtime:3.1.1-1")
}
```

## Version

| Version | Kawa (git describe) | Source | Notes |
|---------|------|--------|-------|
| 3.1.1-1 | 3.1.1-131-g31a0a8755 | Arch Linux `kawa` package | Fixes a `<clinit>` codegen bug (`VerifyError: Bad local variable type`) present in 3.1.1, for modules with keyword-argument-heavy calls at top level under `--module-static-run`. Recommended over 3.1.1. |
| 3.1.1   | 3.1.1-0-gc47de33ad (exact tag) | Built by GNU Guix | Known bug, see 3.1.1-1. Kept published for existing pins; don't add new dependents on this version. |

## Updating

1. Build or obtain the new `kawa.jar`.
2. Place it at `com/momosoftworks/kawa/kawa-runtime/<version>/kawa-runtime-<version>.jar`.
3. Add a matching `.pom` file.
4. Commit and push to `main`.
