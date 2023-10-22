# install-minimina-action

This action installs [Minimina](https://github.com/MinaFoundation/minimina) into your GH workflow. Minimina files are generated under `$MINIMINA_HOME\.minimina`.

## Usage

```yaml
jobs:
  setup-minimina:
    runs-on: ubuntu-latest
    steps:
    - uses: MinaFoundation/install-minimina-action@v1
      with:
        stream: 'stable' # or 'unstable'
```

See [examples.yml](/.github/workflows/examples.yml) workflow for more details.
