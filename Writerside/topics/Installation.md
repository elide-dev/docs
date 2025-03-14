---
switcher-label: OS
---

# Installation

%product% sets up on your machine similar to Node or Python. Use the directions below to install %product%.

## System Requirements

%product% supports **Linux** and **macOS**. **Windows** support is coming soon but is currently considered experimental:

| OS      | Architectures      | Status                                                             | Notes                                                         |
|---------|--------------------|--------------------------------------------------------------------|---------------------------------------------------------------|
| Linux   | `amd64`, `aarch64` | ![Beta](https://img.shields.io/badge/-beta-purple)                 |                                                               |
| macOS   | `amd64`, `aarch64` | ![Beta](https://img.shields.io/badge/-beta-purple)                 | Limited support for certain features, see _macOS Limitations_ |
| Windows | `amd64`            | ![Experimental](https://img.shields.io/badge/-experimental-orange) | Reach out for install instructions                            |

## Installing %product%

<tabs switcher-key="Posix">
    <tab title="One-line Script">
        <code-block lang="bash">curl -sSL --tlsv1.2 elide.sh | bash -s -</code-block>
        <p>The installer script can take options:</p>
        <br />
        <code-block lang="bash">curl -sSL --tlsv1.2 elide.sh | bash -s - --help</code-block>
    </tab>
    <tab title="Package Managers">
        <procedure title="Install with a Package Manager" id="install-with-pkg-manager-posix">
            <step>
                <p>Start typing and select a procedure type from the completion suggestions:</p>
                <img src="completion_procedure.png" alt="completion suggestions for procedure" border-effect="line"/>
            </step>
            <step>
                <p>Press <shortcut>Tab</shortcut> or <shortcut>Enter</shortcut> to insert the markup.</p>
            </step>
        </procedure>
    </tab>
    <tab title="Binary Download">
        <procedure title="Manual Binary Installation" id="binary-download-posix">
            <step>
                <p>Start typing and select a procedure type from the completion suggestions:</p>
                <img src="completion_procedure.png" alt="completion suggestions for procedure" border-effect="line"/>
            </step>
            <step>
                <p>Press <shortcut>Tab</shortcut> or <shortcut>Enter</shortcut> to insert the markup.</p>
            </step>
        </procedure>
    </tab>
</tabs>

<tabs switcher-key="Windows">
    <tab title="Binary Download">
        <procedure title="Manual Binary Installation" id="binary-download-windows">
            <step>
                <p>Start typing and select a procedure type from the completion suggestions:</p>
                <img src="completion_procedure.png" alt="completion suggestions for procedure" border-effect="line"/>
            </step>
            <step>
                <p>Press <shortcut>Tab</shortcut> or <shortcut>Enter</shortcut> to insert the markup.</p>
            </step>
        </procedure>
    </tab>
</tabs>

<procedure title="Testing your installation of %product%" id="post-install-test">
    <step>
        <p>Make sure %product% is on your PATH</p>
        <code-block lang="console">
          > which elide
          /some/path/to/elide
        </code-block>
    </step>
    <step>
        <p>Run --help:</p>
        <code-block lang="console">
          > elide --help
          /some/path/to/elide
        </code-block>
        <img src="bin-help.png" alt="Help output from the %product% binary" border-effect="line"/>
    </step>
</procedure>

## Troubleshooting

Follow the steps below if you're having trouble installing %product%:

<procedure id="install-troubleshooting">
    <step>
        <p>Make sure %product% is on your PATH</p>
        <code-block lang="console">
          > which elide
          /some/path/to/elide
        </code-block>
    </step>
    <step>
        <p>Make sure you have the right binary for your OS and architecture</p>
        <code-block lang="console">
          > file `which elide`
          /some/path/to/elide: Mach-O 64-bit executable arm64
        </code-block>
        <p>Note that on Linux you should see an ELF binary.</p>
    </step>
</procedure>

## Container Images

%product% ships as container images, too. You can use %product% from Docker:

```Console
docker run --rm -it ghcr.io/elide-dev/elide
```

> Read more about container images provided by %product% on the [Container Images](Container-Images.md) page.

## Known Limitations

On certain OS or OS/arch pairs, %product% may not have full support for every feature. Consult the sections below for
the operating system and architecture you want to use.

### Limitations on macOS

Certain features are not supported on macOS yet:

- **G1 garbage collector is not supported**:
  On macOS, the [`serial`](https://www.graalvm.org/latest/reference-manual/native-image/optimizations-and-performance/MemoryManagement/#serial-garbage-collector)
  collector is used instead. This is fine for development but less suitable for production use. This limitation is
  expected to change eventually.

- **Espresso (JVM) is not supported**:
  At this time there are no native libs available upstream for Espresso on macOS.
  Espresso ([Java on Truffle](https://www.graalvm.org/latest/reference-manual/java-on-truffle/)) is experimental and
  this limitation is expected to change eventually.

## Framework Installation

To use %product% as a JVM framework, see the [%product% Framework](Elide-Framework.md) docs. Generally speaking, library
modules are installed as Maven dependencies.

<seealso>
    <category ref="gettingStarted">
        <a href="GettingStarted.md">Getting Started with %product%</a>
        <a href="Polyglot.md">Polyglot 101: Thinking in Multiple Languages</a>
        <a href="Language-Guides.topic">%product% Runtime: Language Guides</a>
        <a href="Elide-Framework.md">%product% Framework: Using %product% from JVM</a>
    </category>
</seealso>
