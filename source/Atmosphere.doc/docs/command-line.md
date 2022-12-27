# Atmosphere Command-Line tool

Atmosphere Command-Line tool can do the most of the things the main application can do, such as analyzing service description, install extensions, and run automated test projects.

The command line tool `atmocli.exe` for Windows or `atmocli` for Linux and MacOS can be found in your installation folder. In general the command line is similar as following:
```batch
atmocli <-switch> [argument] [options]
```
The detailed explanation and available options for each functionality can be found below.

> [!WARNING]
> If an argument or an option contains space charactor, it must be enclosed in quotes, that is: 
> Double quotation marks " under Windows platform. and Simple quotation marks ' under Linux or MacOS

## Functionalities provided by command line tool
In the current version of Atmosphere command line tool, you can perform following tasks:
* Run a automated test project
* Analyze service description, generate and publish extension packages.
* Install an extension package localy or from

## Run automated test project
This functionalety allows to launch an automated test project, use the switch **-run** and provide an test automation project file as argument.
```batch
atmocli -run <project-file> [options]
```

### Argument:
`<project-file>`: The filename of an test automation project file (*.aprj), with full qualified path or relative path to current working directory.

### Options:
Following options can be used with switch `-run`, multiple options can be used simultaneously

* `-out <path>`: **Full qualified Path** or **Relative path to project file** to store the generated test report. short form: `-o`
* `-env <test_environment>`: The test environment to be used for test execution.
* `-env-file <environment_file>`: Overload test environement variables from an external JSON formatted file (for example: to test production environment using existing automation project). Short form: `-ef`
* `-env-password <password>`: If environment variables file is protected with password. You need to provide this password here. Short form: `-ep`
* `-junit`: In supplement of default test report, genrate a JUnit XML format test report. (usually to intergrate with DevOps platforms). The JUnit report will be generated in the same output folder. short form: `-j`
* `-ext <extension_package>`: The extension package `*.pkg` to be loaded before the test execution. Test runner will load provided extension but won't install it. Multiple `-ext` options can be accepted.
* `-key <encryption_key>`: Apply the project encryption key if your automation project is protected. Short form: `-k`
* `-config <config_file>`: The configuration file to be used for the test execution. Short form: `-c`

> [!IMPORTANT]
> Keep the encryption key private for the safety of your system under test. Even if it is not an production environment.
> When running test automation project on a DevOps platform, make sure to apply the best practices to pass the encryption key.


## Analyze service description
This function analyze service description such as OpenAPI Specification and WSDL and generate extension packages.

```batch
atmocli -analyze <service-description> [options]
```
### Argument:
`<service-description>`: The URL or Path of a service description document.

Following documents are supported:
- OpenAPI 2.0 Specification (Swagger) in JSON Format, for example: `swagger.json`
- OpenAPI 3.0 specification in JSON or YAML format
- WSDL (Web Service Description Language) for SOAP 1.1 and SOAP 1.2 Web Services

### Options:
* `-type <type>`: provides the type of the service, possible values are: `OpenAPI`, `SOAP`. Short form: `-t`
* `-app-name <application-name>`: The name of the system under test (for classification and organization of available services). Short form: `-an`
* `-sevice-name <service-name>`: The name of the service in the system under test (for classification and organization of available services). Short form: `-sn`
* `-namespace <namespace>`: provides the namespace of generated code from the description. Short Form: `-ns`
* `-out <path>`: [Optional] **Full qualified Path** or **Relative path to project file** to store the generated extension package.
* `-version <version>`: [Optional] The version of the generated package. For example: `1.2.0`. Short form: `-v`.
If version is not provided, A current date-time based version will be applied.

## Install Extension
This function installs an extension from remote repository or local package file.
```batch
atmocli -install <extension-package-file>|<extension-id> [options]
```
### Argument:
`<extension-package-file>`: The path to an extension package file (`*.pkg`).

`<extension-id>`: The ID of an extension available in an remote repository

### Options:
* `-version <version>`: [optional] The version of the package to be installed. used only when intalling extension from repository. If no version is provided, then command line tool will install the latest stable version.
* `-repo <repository>`: [optional] The extension hub to be used for installation. If no repository is provided, the package will be installed from public repo.

> [!NOTE]
> Companies and Organization with Enterprise Licensing can setup private extension hub. To install extensions to private extension hub, the current system must have a Enterprise license. Only organization approved account can publish extensions to private extension hub.


## Publish an Extension
This function publishs an extension package to Extension hub

```batch
atmocli -publish <extension-package-file> [options]
```
### Argument:
`<extension-package-file>`: The path to an extension package file (`*.pkg`).

### Options:
* `-repo <repository>`: [optional] The extension hub to be used for installation. If no repository is provided, the package will be installed from public repo.

## Install a License
This function installs a license from the given license file.

```batch
atmocli -license <license-file>
```

### Argument:
`<license-file>`: The license file to be installed on your system.

## Show help information
This command line shows the help information 
```batch
atmocli -help
```

