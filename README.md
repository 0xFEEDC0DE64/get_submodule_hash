# get_submodule_hash
GitHub action to get the hash of a submodule

## Example workflow

```yaml
name: Getting the hash of the corelib submodule

on: push

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    - name: Get submodule hash
      id: get-submodule-hash
      uses: 0xFEEDC0DE64/get_submodule_hash
      with:
        submodule: libs/corelib

    - name: Print submodule hash
      run: echo "hash of submodule is ${{ steps.get-submodule-hash.outputs.hash }}"
```
