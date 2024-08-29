Awesome Java App
================

Non-functional example Java application project intended as a specimen for dependency scanning analysis.

The app contains a single, deliberately outdated, dependency, [Stanford CoreNLP](https://stanfordnlp.github.io/CoreNLP/), at [v4.3.2](https://mvnrepository.com/artifact/edu.stanford.nlp/stanford-corenlp/4.3.2), due to its interesting properties (various transitive dependencies, licenses, and vulnerabilities).

Prerequisites
-------------

A JDK is required, recommend at least Java 17.
A great way to manage JDK installations is [SDKMAN!](https://sdkman.io/).

Assembly
--------

Run

    ./gradlew installDist

to assemble and "install" a distribution of the app under `build/install`.
The dependency JARs will be included under `build/install/awesome-java-app/lib`.

SBOM
----

Run

    ./gradlew cyclonedxBom

to generate an SBOM from the runtime classpath dependency tree, in CycloneDX JSON format.
The SBOM file will be created at `build/reports/bom.json`.
