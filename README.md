# `esxl/action-package-build`

A [GitHub Action](https://docs.github.com/en/actions) that contains steps for building EcmaScript based packages.

## Table of contents

<details><summary> Click to expand table of contents</summary>

- [`esxl/action-package-build`](#esxlaction-package-build)
  - [Table of contents](#table-of-contents)
  - [Use](#use)
  - [Configure](#configure)
  </details>

## Use

1. Create a new file, for example _build.yaml_, in the _.github/workflows/_ directory:

   ```bash
   touch ~/.github/workflows/build.yaml
   ```

1. Add the following to the file you just created:

   ```yaml
   name: Build

   env:
     CI: true

   on:
     pull_request:
       branches: [main]

     push:
       branches: [main]

   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - uses: esxl/action-package-build@v0.3.0
   ```

## Configure

This workflow uses the [setup-node](https://github.com/actions/setup-node#readme) action and accepts all of its inputs. See `action/setup-node`'s [action.yaml](https://github.com/actions/setup-node/blob/main/action.yml) for more details.

See this repository's [action.yaml](./action.yaml) file for documentation on additional inputs.
