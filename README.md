# Padok Baywatch Fourkeys Action

This action pushes commit and deployment events to the [Padok Baywatch Fourkeys](https://fourkeys.baywatch.padok.fr) service. For you to monitor the [key DevOps metrics](https://github.com/dora-team/fourkeys) of your GitHub repositories.

## Inputs

| name      | required | type   | default | description                                              |
| --------- | -------- | ------ | ------- | -------------------------------------------------------- |
| metadatas | no       | string | "{}"    | Metadata key values to sort data in the Fourkeys Metrics |

## Example usage

Workflow:

```yml
name: Publish Data to Padok Baywatch Fourkeys
on:
  push:
    branches: [ master ]
jobs:
  publish:
    runs-on: ubuntu-latest
    permissions:
      contents: read
      id-token: write
    steps:
    - name: Publish Data to Padok Baywatch Fourkeys
      uses: padok-team/baywatch-fourkeys-action@v1
```

## License

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
