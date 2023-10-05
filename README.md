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
    steps:
    - uses: actions/checkout@v2
      with:
        fetch-depth: 0
    - name: Publish Data to Padok Baywatch Fourkeys
      uses: padok-team/baywatch-fourkeys-action@main
```
