# Install Extensions
This function installs an extension from remote repository or local package file.
```batch
atmocli -install <extension-package-file>|<extension-id> [options]
```
## Argument:
`<extension-package-file>`: The path to an extension package file (`*.pkg`).

`<extension-id>`: The ID of an extension available in an remote repository

## Options:
* `-version <version>`: [optional] The version of the package to be installed. used only when intalling extension from repository. If no version is provided, then command line tool will install the latest stable version.
* `-repo <repository>`: [optional] The extension hub to be used for installation. If no repository is provided, the package will be installed from public repo.

> [!NOTE]
> Companies and Organization with Enterprise Licensing can setup private extension hub. To install extensions to private extension hub, the current system must have a Enterprise license. Only organization approved account can publish extensions to private extension hub.