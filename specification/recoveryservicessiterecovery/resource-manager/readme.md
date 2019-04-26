# RecoveryServicesSiteRecovery

> see https://aka.ms/autorest

This is the AutoRest configuration file for RecoveryServicesSiteRecovery.

---

## Getting Started

To build the SDK for RecoveryServicesSiteRecovery, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`

---

## Configuration

### Basic Information

These are the global settings for the RecoveryServicesSiteRecovery API.

``` yaml
openapi-type: arm
tag: package-2018-07
```


### Tag: package-2018-07

These settings apply only when `--tag=package-2018-07` is specified on the command line.

```yaml $(tag) == 'package-2018-07'
input-file:
  - Microsoft.RecoveryServices/stable/2018-07-10/service.json
```
### Tag: package-2016-08

These settings apply only when `--tag=package-2018-01` is specified on the command line.

``` yaml $(tag) == 'package-2018-01'
input-file:
- Microsoft.RecoveryServices/stable/2018-01-10/service.json
```

### Tag: package-2016-08

These settings apply only when `--tag=package-2016-08` is specified on the command line.

``` yaml $(tag) == 'package-2016-08'
input-file:
- Microsoft.RecoveryServices/stable/2016-08-10/service.json
```

---

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-node
  - repo: azure-sdk-for-ruby
    after_scripts:
      - bundle install && rake arm:regen_all_profiles['azure_mgmt_recovery_services_site_recovery']
```

## C#

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  payload-flattening-threshold: 0
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.RecoveryServices.SiteRecovery
  output-folder: $(csharp-sdks-folder)/RecoveryServices.SiteRecovery/Management.RecoveryServices.SiteRecovery/Generated
  clear-output-folder: true
```

## Go

See configuration in [readme.go.md](./readme.go.md)

## Java

These settings apply only when `--java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-libraries-for-java clone>`.

``` yaml $(java)
azure-arm: true
fluent: true
namespace: com.microsoft.azure.management.recoveryservicessiterecovery
license-header: MICROSOFT_MIT_NO_CODEGEN
payload-flattening-threshold: 1
output-folder: $(azure-libraries-for-java-folder)/azure-mgmt-recoveryservicessiterecovery
```

### Java multi-api

``` yaml $(java) && $(multiapi)
batch:
  - tag: package-2016-08
```

### Tag: package-2016-08 and java

These settings apply only when `--tag=package-2016-08 --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2016-08' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.recoveryservicessiterecovery.v2018_01_10
  output-folder: $(azure-libraries-for-java-folder)/recoveryservicessiterecovery/resource-manager/v2018_01_10
regenerate-manager: true
generate-interface: true
```