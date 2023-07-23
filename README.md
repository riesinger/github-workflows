# GitHub Actions Workflows

This is a collection of workflows and scripts for GitHub Actions. I use these in a couple of other repositories.

## Workflows

### `build-docker.yml`

This builds a docker image from a `Dockerfile` and tags it following SemVer.

<details>
<summary>Usage example:</summary>

```yaml
name: CI

on:
  push:

jobs:
  build:
    uses: riesinger/github-workflows/.github/workflows/build-docker.yml@main
    with:
      image-name: name-of-image # yields ghcr.io/riesinger/name-of-image
    secrets: inherit
```

</details>
