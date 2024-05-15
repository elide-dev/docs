---
switcher-label: Gradle Dialect
---

# Elide Base

<tldr>
    <p>Baseline multi-platform utilities</p>
    <p columns="2">
        <img style="inline" src="https://img.shields.io/badge/status-beta-purple" />
        <img style="inline" src="https://img.shields.io/badge/platforms-all-white" />
    </p>
    <a target="_blank" href="https://docs.elide.dev/apidocs/packages/base/index.html">API Docs</a>
    <a target="_blank" href="https://search.maven.org/search?q=g:dev.elide%20base">Maven Central</a>
    <br />
    <p><b>Module:</b></p>
    <code>dev.elide:elide-base</code>
    <p><b>Latest:</b></p>
    <code>%version%</code>
</tldr>

Baseline multi-platform utilities, available on all platforms supported by Kotlin. Includes encoding utilities,
annotations, and other code used throughout the %product% framework.

The %product% Base module depends only on Kotlin Stdlib, KotlinX, and [%product% Core](Elide-Core.md).

## What's in the box?

<list>
    <li>Encoders for Hex and Base64</li>
    <li>Cryptography and UUID-gen utilities</li>
</list>

## Usage

<tabs>
    <tab title="Gradle">
        <p switcher-key="Kotlin DSL"><b>Kotlin DSL</b></p>
        <code-block lang="kotlin" switcher-key="Kotlin DSL">
        implementation("dev.elide:elide-base:%version%")
        </code-block>
        <p switcher-key="Kotlin DSL"><b>Kotlin DSL</b> (%product% Catalog)</p>
        <code-block lang="kotlin" switcher-key="Kotlin DSL">
        implementation(framework.elide.base)
        </code-block>
        <p switcher-key="Groovy DSL"><b>Groovy DSL</b></p>
        <code-block lang="groovy" switcher-key="Groovy DSL">
        implementation "dev.elide:elide-base:%version%"
        </code-block>
        <p switcher-key="Groovy DSL"><b>Groovy DSL</b> (%product% Catalog)</p>
        <code-block lang="groovy" switcher-key="Groovy DSL">
        implementation framework.elide.base
        </code-block>
        <p><b>Version Catalog</b></p>
        <code-block lang="text">
        elide-base = { module = "dev.elide:elide-base", version.ref = "elide" }
        </code-block>
    </tab>
    <tab title="Maven">
        <b>Gradle</b>
    </tab>
    <tab title="Bazel">
        <b>Bazel</b>
    </tab>
</tabs>
