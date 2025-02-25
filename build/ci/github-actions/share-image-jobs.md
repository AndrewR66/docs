---
title: Share built image between jobs with GitHub Actions
keywords: ci, github actions, gha, buildkit, buildx
---

As each job is isolated in its own runner, you can't use your built image
between jobs, except if you're using [self-hosted runners](https://docs.github.com/en/actions/hosting-your-own-runners/about-self-hosted-runners){:target="blank" rel="noopener" class=""}
However, you can [pass data between jobs](https://docs.github.com/en/actions/using-workflows/storing-workflow-data-as-artifacts#passing-data-between-jobs-in-a-workflow){:target="blank" rel="noopener" class=""}
in a workflow using the [actions/upload-artifact](https://github.com/actions/upload-artifact){:target="blank" rel="noopener" class=""}
and [actions/download-artifact](https://github.com/actions/download-artifact){:target="blank" rel="noopener" class=""}
actions:

{% raw %}
```yaml
name: ci

on:
  push:
    branches:
      - "main"

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      -
        name: Checkout
        uses: actions/checkout@v3
      -
        name: Set up Docker Buildx
        uses: docker/setup-buildx-action@v2
      -
        name: Build and export
        uses: docker/build-push-action@v4
        with:
          context: .
          tags: myimage:latest
          outputs: type=docker,dest=/tmp/myimage.tar
      -
        name: Upload artifact
        uses: actions/upload-artifact@v3
        with:
          name: myimage
          path: /tmp/myimage.tar

  use:
    runs-on: ubuntu-latest
    needs: build
    steps:
      -
        name: Download artifact
        uses: actions/download-artifact@v3
        with:
          name: myimage
          path: /tmp
      -
        name: Load image
        run: |
          docker load --input /tmp/myimage.tar
          docker image ls -a
```
{% endraw %}
