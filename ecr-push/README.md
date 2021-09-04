# An action to push an image to ECR

## How to use

- Workflow will work only if this action is called in a workflow with following setup:

```yaml
on:
  push:
    tags:
      - v[0-9]+.[0-9]+.[0-9]+
```

- No need to to explicitly use `actions/checkout@v2`, since it is baked into the action.

- A repository name and region should be provided as an input in the following format

```yaml
...
steps:
    ...
    - uses: LinkerApplication/ecr-push@v1
    with:
        repo-name: 'your-repo-name'
        repo-region: 'xx-xx-x'
        # Optionally a dynamic tag name which will also be pushed to the repository
        # can be specified. Default is `current-dev`
        dynamic-tag-name: 'dynamic-tag-name'
    ...
```
