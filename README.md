# Eirbware's workflows

This repository contains all reusable workflows and workflow templates to provide better CICD

## How to use reusable workflows

To use a reusable workflow, you have to make a job which calls it, like this:
```yaml
  build-and-push:
    uses: Eirbware/.github/.github/workflows/build-and-publish.yml@master
    with:
      file: "./Dockerfile"
      image_name: ${{ github.repository }}
    secrets: 
      registry_username: ${{ secrets.registry_username }}
      registry_api_key: ${{ secrets.registry_api_key }}
```

More information [here](https://docs.github.com/en/actions/how-tos/reuse-automations/reuse-workflows)
