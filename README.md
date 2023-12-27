# @riscv-forks/electron-builder

electron-builder with riscv64 support.

## Usage

Override the dependency resolution of the following packages:

```
app-builder-lib -> @riscv-forks/app-builder-lib
builder-util -> @riscv-forks/builder-util
electron-builder -> @riscv-forks/electron-builder
```

## Maintenance

For each new electron-builder release, the following steps should be performed:

1. Switch to tag of upstream release
2. Pick up riscv commits from riscv64 branch
3. Run `pnpm i` and `pnpm compile`
4. Push the current HEAD to a new branch named after the upstream release, e.g. `v24.10.0-riscv`
5. Publish to npm: `pnpm -F <package_dir_name> publish --access public`

## Note

When electron officially supports riscv64, this package should be deprecated and removed.
