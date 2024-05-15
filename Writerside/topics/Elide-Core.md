---
switcher-label: Gradle Dialect
---

# Elide Core

<tldr>
    <p>Core utilities and annotations</p>
    <p columns="2">
        <img style="inline" src="https://img.shields.io/badge/status-beta-purple" />
        <img style="inline" src="https://img.shields.io/badge/platforms-all-white" />
    </p>
    <a target="_blank" href="https://docs.elide.dev/apidocs/packages/core/index.html">API Docs</a>
    <a target="_blank" href="https://search.maven.org/search?q=g:dev.elide%20core">Maven Central</a>
    <br />
    <p><b>Module:</b></p>
    <code>dev.elide:elide-core</code>
    <p><b>Latest:</b></p>
    <code>%version%</code>
</tldr>

Core utilities and annotations which are applicable on all platforms, and which support all targets available from
Kotlin Multiplatform (Linux, macOS, Windows, JVM, WASM, JavaScript, etc.).

Core depends only on Kotlin Stdlib and KotlinX.

## What's in the box?

<list>
    <li>Encoders for Hex and Base64</li>
    <li>Annotations used throughout %product% and guest apps</li>
</list>

## Usage

<tabs>
    <tab title="Gradle">
        <p switcher-key="Kotlin DSL"><b>Kotlin DSL</b></p>
        <code-block lang="kotlin" switcher-key="Kotlin DSL">
        implementation("dev.elide:elide-core:%version%")
        </code-block>
        <p switcher-key="Kotlin DSL"><b>Kotlin DSL</b> (%product% Catalog)</p>
        <code-block lang="kotlin" switcher-key="Kotlin DSL">
        implementation(framework.elide.core)
        </code-block>
        <p switcher-key="Groovy DSL"><b>Groovy DSL</b></p>
        <code-block lang="groovy" switcher-key="Groovy DSL">
        implementation "dev.elide:elide-core:%version%"
        </code-block>
        <p switcher-key="Groovy DSL"><b>Groovy DSL</b> (%product% Catalog)</p>
        <code-block lang="groovy" switcher-key="Groovy DSL">
        implementation framework.elide.core
        </code-block>
        <p><b>Version Catalog</b></p>
        <code-block lang="text">
        elide-core = { module = "dev.elide:elide-core", version.ref = "elide" }
        </code-block>
    </tab>
    <tab title="Maven">
        <b>Gradle</b>
    </tab>
    <tab title="Bazel">
        <b>Bazel</b>
    </tab>
</tabs>
