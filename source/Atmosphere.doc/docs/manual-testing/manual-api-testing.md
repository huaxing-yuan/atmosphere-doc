# Manual API Testing
**API** or **Web Service** Testing is an important part in software testing process.
These tests are generally performed before *Integration Test* or *End-to-End Test*, once a functionality has been implemented in a component. 

API Testing can be performed:
- Manually, generally focused for new API or for new features of existing API.
- Or Automatically, which we will build an automation project with different test steps (to perform actions) with assertions (to verify expected results).

In this section we will focus on Manual API Tesing feature of Atmosphere Studio.

To use Manual API Testing feature of `Atmosphere Studio`, select `Manual API Testing` from main menu or home page.
![Menu Manual Api Testing](../../images/menu-manual-api-testing.png)


## Workspace for Manual API Testing
Now let's get familiar with your workspace for Manual API Testing
[REVIEW: SCREENSHOT OF MANUAL API TESTING]

- `Available APIs` lists all your API to test. Each API is organized in an Application. (Your application under test may have multiple API)
- `Request Editor` helps you to build test data with Atmosphere Studio's unique `Object-model based` API testing technology.

> [!NOTE]
> To understand `Object-model based` API Testing, please refer to [Object-model based API Testing](../features/object-model-based-testing.md)

> [!CAUTION]
> To understand `Object-model based` API Testing, please refer to [Object-model based API Testing](../features/object-model-based-testing.md)

> [!WARNING]
> To understand `Object-model based` API Testing, please refer to [Object-model based API Testing](../features/object-model-based-testing.md)


## API Definition
In order to perform tests on a particular API, we need its definition, so the service provider and the service consumer can understand each other.
API definition usually contains the data structure, network protocol, endpoints and other useful information.
With Atmophere Studio you can import most widely used API definitions, such as `WSDL`, `OpenAPI Specification` and `OData CSDL`.

Reference: [Import API Definition](import-api-definition.md)

## Request Editor

Reference: [Request Editor](request-editor.md)

## Save preferred Requests
Reference: [Saved Requests](saved-requests.md)

## Request Options
Reference: [Request Options](request-options.md)

## Use Test Environments
Reference: [Test Environments](test-environments.md)