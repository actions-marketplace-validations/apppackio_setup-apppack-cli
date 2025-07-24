# Setup AppPack CLI GitHub Action

This action downloads the [AppPack](https://apppack.io) CLI from the [GitHub releases page](https://github.com/apppackio/apppack/releases).

## Inputs

### `version`

**Optional** Defaults to `latest`

## Outputs

### `version`

The version of the CLI that was setup

## Example usage

```yaml
- name: AppPack CLI
  uses: apppackio/setup-apppack-cli@v1
```

### With GitHub Token (Optional)

If you encounter GitHub API rate limit errors (403), you can provide a GitHub token:

```yaml
- name: AppPack CLI
  uses: apppackio/setup-apppack-cli@v1
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

This increases the rate limit from 60 to 5,000 requests per hour.
