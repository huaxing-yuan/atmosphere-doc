# Publish an Extension
This function publishs an extension package to Extension hub

```batch
atmocli -publish <extension-package-file> [options]
```
## Argument:
`<extension-package-file>`: The path to an extension package file (`*.pkg`).

## Options:
* `-repo <repository>`: [optional] The extension hub to be used for installation. If no repository is provided, the package will be installed from public repo.