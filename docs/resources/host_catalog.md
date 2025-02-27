---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "boundary_host_catalog Resource - terraform-provider-boundary"
subcategory: ""
description: |-
  The host catalog resource allows you to configure a Boundary host catalog. Host catalogs are always part of a project, so a project resource should be used inline or you should have the project ID in hand to successfully configure a host catalog.
---

# boundary_host_catalog (Resource)

The host catalog resource allows you to configure a Boundary host catalog. Host catalogs are always part of a project, so a project resource should be used inline or you should have the project ID in hand to successfully configure a host catalog.

## Example Usage

```terraform
resource "boundary_scope" "org" {
  name                     = "organization_one"
  description              = "My first scope!"
  scope_id                 = boundary_scope.global.id
  auto_create_admin_role   = true
  auto_create_default_role = true
}

resource "boundary_scope" "project" {
  name                   = "project_one"
  description            = "My first scope!"
  scope_id               = boundary_scope.org.id
  auto_create_admin_role = true
}

resource "boundary_host_catalog" "example" {
  name        = "My catalog"
  description = "My first host catalog!"
  type        = "Static"
  scope_id    = boundary_scope.project.id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **scope_id** (String) The scope ID in which the resource is created.
- **type** (String) The host catalog type. Only `static` is supported.

### Optional

- **description** (String) The host catalog description.
- **name** (String) The host catalog name. Defaults to the resource name.

### Read-Only

- **id** (String) The ID of the host catalog.

## Import

Import is supported using the following syntax:

```shell
terraform import boundary_host_catalog.foo <my-id>
```
