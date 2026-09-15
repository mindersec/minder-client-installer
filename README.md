# Minder Client Installer GitHub Action

This action installs the Minder client on the runner.

## Usage

```yaml
jobs:
  install-minder:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v7.0.1
    # We need cosign to verify the Minder client
    - uses: sigstore/cosign-installer@v4.1.2
    # Install the Minder client
    - uses: mindersec/minder-client-installer@v1.1.3  # Pin this to a SHA
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
