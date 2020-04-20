## AZ

These settings apply only when `--az` is specified on the command line.

``` yaml $(az)
az:
  extensions: hybridcompute
  package-name: azure-mgmt-hybridcompute
  namespace: azure.mgmt.hybridcompute
az-output-folder: $(azure-cli-extension-folder)/src/hybridcompute
python-sdk-output-folder: "$(az-output-folder)/azext_hybridcompute/vendored_sdks/hybridcompute"
directive:
  - from: HybridCompute.json
    where: $.definitions.Machine.properties.properties
    transform: $['x-ms-client-name'] = "properties"
  - from: HybridCompute.json
    where: $.definitions.OperationValue.properties.display
    transform: $['x-ms-client-name'] = "display"
  - from: HybridCompute.json
    where: $.definitions.MachineUpdate.properties.properties
    transform: $['x-ms-client-name'] = "updateProperties"
  - from: HybridCompute.json
    where: $.definitions.MachineReconnect.properties.properties
    transform: $['x-ms-client-name'] = "ReconnectProperties"
  - from: HybridCompute.json
    where: $.definitions.MachineExtension.properties.properties
    transform: $['x-ms-client-name'] = "ExtensionProperties"
  - from: HybridCompute.json
    where: $.definitions.MachineExtensionUpdate.properties.properties
    transform: $['x-ms-client-name'] = "extensionUpdateProperties"
```
