# Extension for GitQ chrome plugin

> name: Duplicate code

on: pull_request

jobs:
  duplicate-code-check:
    name: Check for duplicate code
    runs-on: ubuntu-20.04
    steps:
      - name: Check for duplicate code
        uses: platisd/duplicate-code-detection-tool@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          directories: "."
