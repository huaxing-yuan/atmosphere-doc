# Atmosphere Command-Line tool

Atmosphere Command-Line tool can do the most of the things the main application can do, such as analyzing service description, install extensions, and run automated test projects.

The command line tool `atmocli.exe` for Windows or `atmocli` for Linux and MacOS can be found in your installation folder. In general the command line is similar as following:
```batch
atmocli <-switch> [argument] [options]
```
The detailed explanation and available options for each functionality can be found below.

Possible switches are:
- `-run`: execute an automation project, by providing project files and other arguments.
- `-analyze`: analyses an service description such as OpenAPI Specification (Swagger) or WSDL and generate service extension pack.
- `-install`: install a service extension pack, localy or from Extension Hub.
- `-publish`: publishes a service extension pack to public or private Extension Hub.
- `-license`: install or reconfigure your license settings.
- `-help`: displays the help information.

> [!WARNING]
> If an argument or an option contains space charactor, it must be enclosed with quotation marks. Under `Windows` platform, use double-quote `"`, while under `MacOS` and `Linux` use simple quote `'`.

For more information about each functionality, please refers to following topics:
- [Run automated test project](run-automated-tests.md)
- [Analyze service Description](analyze-service-description.md)
- [Install extensions](install-extensions.md)
- [Publish extensions](publish-extensions.md)
- [Configure License](configure-license.md)



## Show help information
This command line shows the help information 
```batch
atmocli -help
```

