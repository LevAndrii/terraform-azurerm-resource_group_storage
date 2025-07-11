# Module Overview

This Terraform module deploys:

- A resource group
- A storage account

## Requirements

- Terraform installed
- Azure CLI or appropriate credentials configured

## Input Variables

| Variable              | Description                    | Type   |
|-----------------------|--------------------------------|--------|
| `rg_name`             | Name of the resource group     | string |
| `rg_location`        | Location for the resource group | string |
| `storage_account_name` | Name of the storage account    | string |

## Usage Example

```hcl
module "basic_resources" {
  source               = "./path_to_module"
  rg_name              = "example-rg"
  rg_location          = "West Europe"
  storage_account_name = "examplestorageacct"
}
```

## Outputs

- `rg_id`: ID of the created resource group
- `storage_account_id`: ID of the created storage account

## Steps to Deploy

```bash
terraform init
terraform plan
terraform apply
```

Type `yes` when prompted to confirm.
