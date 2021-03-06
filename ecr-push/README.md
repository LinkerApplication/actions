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

- A repository name, region and AWS credentials should be provided as an input in the following format

```yaml
...
steps:
    ...
    - uses: LinkerApplication/actions/ecr-push@v1
      with:
        repo-name: 'your-repo-name'
        repo-region: 'xx-xx-x'
        aws-access-key-id: 'xxxxxxxxxxxxxxxxxx'
        aws-secret-access-key: 'xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx'
        # Optionally a dynamic tag name which will also be pushed to the repository
        # can be specified. Default is `current-dev`
        dynamic-tag-name: 'current-dev'
    ...
```
