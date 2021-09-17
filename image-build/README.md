# An action to build an image

## How to use

- No need to to explicitly use `actions/checkout@v2`, since it is baked into the action.

- Resulting image name should be provided as a `image-name` parameter.

- Tag name parameter `image-tag` is optional. Default is `testing`

- Context path parameter `context` is optional. Default is `.`

- Dockerfile name parameter `dockerfile-name` is optional. Default is `Dockerfile`

```yaml
...
steps:
    ...
    - uses: LinkerApplication/actions/image-build@v1
      with:
          image-name: 'your-image-name'
          # Following parameters are optional
          image-tag: 'testing'
          context: `.`
          dockerfile-name: `Dockerfile`
    ...
```
