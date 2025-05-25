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
            <p>Elide is not available yet via package managers. Please check back soon.</p>
        </procedure>
    </tab>
    <tab title="Binary Download">
        <procedure title="Manual Binary Installation" id="binary-download-posix">
            <step>
                <p>Binary downloads are available via GitHub releases:</p>
                <a href="https://github.com/elide-dev/elide/releases">GitHub Releases</a>
            </step>
        </procedure>
    </tab>
</tabs>

<tabs switcher-key="Windows">
    <tab title="Binary Download">
        <procedure title="Manual Binary Installation" id="binary-download-windows">
            <step>
                <p>Elide is not supported yet on Windows.</p>
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

## Container Images

%product% ships as container images, too. You can use %product% from Docker:

```Console
docker run --rm -it ghcr.io/elide-dev/bash
```

## Continuous Integration

%product% ships a [GitHub action](https://github.com/marketplace/actions/setup-elide):

```yaml
  - name: "Setup: Elide"
    uses: elide-dev/setup-elide@v2
    with:
      # any tag from the `elide-dev/releases` repo.
      # omit a version to use the latest version.
      version: 1.0.0-beta3
```

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
