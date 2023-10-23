# `install-minimina-action`

This GitHub action facilitates the installation of [Minimina](https://github.com/MinaFoundation/minimina) within your GitHub workflow. Upon successful execution, Minimina files are stored at `$MINIMINA_HOME\.minimina`.

## 📖 Usage

### 1. Installing from a Package Stream
To install Minimina as a `.deb` package from a predefined stream:

```yaml
jobs:
  setup-minimina:
    runs-on: ubuntu-latest
    steps:
    - uses: MinaFoundation/install-minimina-action@v1
      with:
        stream: 'stable'  # Options: 'stable' or 'unstable'; if param ommited it will install 'stable'
```

### 2. Building from a Specific Commit or Branch
To install and build Minimina directly from a given commit hash or branch:

```yaml
jobs:
  setup-minimina:
    runs-on: ubuntu-latest
    steps:
    - uses: MinaFoundation/install-minimina-action@v1
      with:
        commit_or_branch: 'main'  # Replace 'main' with your desired commit or branch
```

> ⚠️ **Note**: Ensure both Rust and `cargo` are present in your environment when opting to install and build from a commit or branch.

For a more comprehensive guide and additional examples, please refer to the [examples.yml](/.github/workflows/examples.yml) workflow.