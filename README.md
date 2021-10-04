# Actions for LinkerApplication

> ⚠️ This repository is publicly available, since it does not contain any sensitive information about the project.
> Anyone can copy it, so do not put any actions, which may be harmful in case of use by any unauthorized users.

## Available actions

> Look for detailed documantation in individual action folders.

- `ecr-push` - Push an image to ECR
- `ecs-deploy` - Deploy an application to ECS
- `image-build` - Build an image

## Releasing

To release a new version

- Create a tag `vX.X.X`

```bash
git tag vX.X.X -m "some tag info"
```

- Push that tag to the repository

```bash
git push origin vX.X.X
```

- Update the major version tag `vX` and push it to the repo as well

```bash
git tag vX -m "release info"
git push
```

- Create 2 releases. First with the version of the minor tag, second with the major version tag.
