# Minder Client Installer GitHub Action

This action installs the Minder client on the runner.

## Usage

```yaml
jobs:
  install-minder:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v4
    # We need cosign to verify the Minder client
    - uses: sigstore/cosign-installer@v3.6.0
    # Install the Minder client
    - uses: github.com/stacklok/minder-client-installer@latest
    # Use it!
    - run: minder --help
```

## Inputs

### `release`

**Optional** The release version of the Minder client to install.

### `install-dir`

**Optional** The directory to install the Minder client to.

### `use-sudo`

**Optional** Whether to use `sudo` when installing the Minder client.
