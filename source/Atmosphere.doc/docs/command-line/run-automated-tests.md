# Run automated test project

This functionalety allows you to launch an automated test project in the command-line interface, it is useful when you are working in a DevOps environment and want to integrate your test process into  CI/CD pipelines. 

To run automated test, use the switch **-run**, provide test automation project file, along with other arguments.
```batch
atmocli -run <project-file> [options]
```

## Argument:
`<project-file>`

Mandatory argument, The filename of an test automation project file (*.aprj), with full qualified path or relative path to current working directory.

## Options:
Following options can be used with switch `-run`, multiple options can be used simultaneously

### `-key <encryption_key>`
Short form: `-k`

Provides project encryption key if automation project is protected. 
> [!IMPORTANT]
> Keep your encryption key secure.
> When running test automation project on a DevOps platform, never store clear encryption key in project repository, pipeline apply the best practices to pass the encryption key.

### `-out <path>`
Short form: `-o`

**Full qualified Path** or **Relative path to project file** to store the generated test report.

### `-env <test_environment>`
In the test automation project you are able to configure one or more Test Environments, where you can store different test parameters, credentials and service Urls. Use this option to target the test against different test environments. 

### `-env-file <environment_file>`
Short form: `-ef`

Overload test environement variables from an external JSON formatted file. For example: if you want to test on production environment, you can store these credentials and secret test parameters in a separate file.

If an environment file is provided, it will override test environments defined in the project specified in `-env` option.


### `-env-password <password>`
Short form: `-ep`

If environment variables file specified with `-env-file` option is protected by password. You'll need to provide this password with this parameter.

### `-junit`
Short form: `-j`

In supplement of default test report, genrates a JUnit XML format test report.
JUnit XML test report is widely supported by DevOps platforms. 

The JUnit report will be generated in the same output folder.

### `-ext <extension_package>`
If test project uses functionalities from special extensions, you need to ensure the availability of these extensions on target machine. With this argument, extension package `*.pkg` will be loaded before the test execution. 

Remarks:
* Test runner will load provided extension but won't install it.
* Multiple `-ext` options can be provided


### `-config <config_file>`
Short form: `-c`

The configuration file to be used for the test execution. 

