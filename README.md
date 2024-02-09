# quarkus-gradle-renovate-example

[![Use this template](https://img.shields.io/badge/from-java--library--template-brightgreen?logo=dropbox)](https://github.com/thriving-dev/java-library-template/generate)
[![Java CI](https://github.com/thriving-dev/quarkus-gradle-renovate-example/actions/workflows/1.pipeline.yml/badge.svg)](https://github.com/thriving-dev/quarkus-gradle-renovate-example/actions/workflows/1.pipeline.yml)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md)

Renovate hit a snag with Quarkus updates?

**TLDR:** Renovate cannot automatically update Quarkus gradle plugin dependencies for projects created via [Quarkus CLI](https://quarkus.io/guides/cli-tooling).
The explanation to the version not tracked is relatively simple ...Renovate cannot resolve the packageName and datasource.

Don't worry! This guide reveals the issue & the solution to fix it.   
=> https://thriving.dev/blog/patch-quarkus-gradle-like-a-pro-with-renovate

## Created using 
```shell script
quarkus create app dev.thriving.example:quarkus-gradle-renovate-example:0.0.1 \
  --gradle-kotlin-dsl \
  --extension='kotlin,resteasy-reactive-jackson'
```

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./gradlew quarkusDev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./gradlew build
```
It produces the `quarkus-run.jar` file in the `build/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `build/quarkus-app/lib/` directory.

The application is now runnable using `java -jar build/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:
```shell script
./gradlew build -Dquarkus.package.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar build/*-runner.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./gradlew build -Dquarkus.package.type=native
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./gradlew build -Dquarkus.package.type=native -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./build/quarkus-gradle-renovate-example-0.0.1-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/gradle-tooling.

## Related Guides

- Kotlin ([guide](https://quarkus.io/guides/kotlin)): Write your services in Kotlin

## Provided Code

### RESTEasy Reactive

Easily start your Reactive RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started-reactive#reactive-jax-rs-resources)

## Credits
- Created by https://github.com/thriving-dev/java-library-template
