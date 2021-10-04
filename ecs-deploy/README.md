# An action to deploy a service to ECS

## How to use

- No need to to explicitly use `actions/checkout@v2`, since it is baked into the action.

## Required paramters

- Cluster region name: `cluster-region`

- Cluster name: `cluster-name`

- Service name, which should be updated: `service-name`

- Task definition name, which should be updated: `task-definition-family-name`

- Task definition filename, in which prodcess of deploymant is described: `task-definition-file-name`

- Name of a repository, where required image lives: `repo-name`

- Name of the image to be deployed: `image-name`

- Specifying the version of an image, which should be deployed: `image-version`. Is optional. Default is latest tag.

```yaml
...
steps:
    ...
    - uses: LinkerApplication/actions/ecs-deploy@v1
      with:
          cluster-region: 'cluster-region'
          cluster-name: 'cluster-name'
          service-name: 'service-name'
          task-definition-family-name: 'task-definition-family-name'
          task-definition-file-name: 'task-definition-file-name'
          repo-name: `repo-name`
          image-name: `image-name`
          # Following parameters are optional
          image-version: `vX.X.X`
    ...
```
