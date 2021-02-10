## AZ

These settings apply only when `--az` is specified on the command line.


``` yaml $(az)

az:
  extensions: marketplace
  package-name: azure-mgmt-marketplace
  namespace: azure.mgmt.marketplace
  disable-checks: true
  client-subscription-bound: false
az-output-folder: $(azure-cli-extension-folder)/src/marketplace
python-sdk-output-folder: "$(az-output-folder)/azext_marketplace/vendored_sdks/marketplace"

directive:
  - where:
      group: marketplace host-pool
    set:
      group: marketplace hostpool
  - where:
      group: marketplace application-group
    set:
      group: marketplace applicationgroup
```
