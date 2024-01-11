# gRPC Library

[Docs](https://yidongnan.github.io/grpc-spring-boot-starter/en/)

# Deploying to JitPack

[JitPack](https://jitpack.io/) is a package repository for JVM and Android projects. It allows you to build and
distribute your Java library or application directly from your GitHub repository.

## Steps:

### 1. Implement desired changes

Make sure the Java project contains a valid `pom.xml` file for Maven projects. Ensure that your
project builds successfully locally. Increase the version of the application in the `pom.xml` for each change.

### 2. Add a release

Create a release for the version you want to deploy. The version of the release should match the version in of the
application in the `pom.xml`. This is the version that JitPack will use. Once the release is created a
`Build and Deploy to JitPack` pipeline will be triggered (it is located in `.github/workflows/jitpack.yml`). When this
pipeline finishes successfully, the new release will be available on the JitPack.

### 3. Navigate to JitPack

Visit [JitPack](https://jitpack.io/) and enter your **_Real-Estate-Ads/grpc-definitions_**. JitPack will automatically
detect the latest
release.

### 4. Get the Dependency

In order to use this dependency in your project, you need to have the JitPack listed as repository, like this:

```xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>
```

JitPack will provide you with the dependency snippet that looks like this:

```xml
<dependency>
    <groupId>com.github.Real-Estate-Ads/groupId>
    <artifactId>grpc-definitions</artifactId>
    <version>{release-version}</version>
</dependency>
