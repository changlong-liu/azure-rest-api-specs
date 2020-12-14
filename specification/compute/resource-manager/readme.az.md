## AZ

These settings apply only when `--az` is specified on the command line.

``` yaml $(az)
az:
  extensions: compute
  namespace: azure.mgmt.compute
  package-name: azure-mgmt-compute
  randomize-names: false
az-output-folder:  $(azure-cli-extension-folder)/src/compute
python-sdk-output-folder: "$(az-output-folder)/azext_compute/vendored_sdks/compute"


cli:
  cli-directive:
    - where:
        group: "*"
      hidden: true
    - where:
        group: CloudService*
      hidden: false
```
