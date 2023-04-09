# Analyze service description
This function analyze service description such as OpenAPI Specification and WSDL and generate extension packages.

```batch
atmocli -analyze <service-description> [options]
```
## Argument:
`<service-description>`: The URL or Path of a service description document.

Following documents are supported:
- OpenAPI 2.0 Specification (Swagger) in JSON Format, for example: `swagger.json`
- OpenAPI 3.0 specification in JSON or YAML format
- WSDL (Web Service Description Language) for SOAP 1.1 and SOAP 1.2 Web Services

## Options:
* `-type <type>`: provides the type of the service, possible values are: `OpenAPI`, `SOAP`. Short form: `-t`
* `-app-name <application-name>`: The name of the system under test (for classification and organization of available services). Short form: `-an`
* `-sevice-name <service-name>`: The name of the service in the system under test (for classification and organization of available services). Short form: `-sn`
* `-namespace <namespace>`: provides the namespace of generated code from the description. Short Form: `-ns`
* `-out <path>`: [Optional] **Full qualified Path** or **Relative path to project file** to store the generated extension package.
* `-version <version>`: [Optional] The version of the generated package. For example: `1.2.0`. Short form: `-v`.
If version is not provided, A current date-time based version will be applied.