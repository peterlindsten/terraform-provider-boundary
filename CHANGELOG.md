## 1.0.5 (September 09, 2021)

### Deprecations/Changes

* Deprecate fields `host_set_ids` and `application_credential_library_ids` of the 
  `target` resource. See boundary 0.5.0 [changelog](https://github.com/hashicorp/boundary/blob/main/CHANGELOG.md#deprecationschanges) for more detail on the deprecation.
  ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/134)).

## 1.0.4 (August 19, 2021)

### New and Improved

* Adds managed groups resource
  ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/118)).

## 1.0.3 (June 30, 2021)

### New and Improved

* Adds credential library resource for Vault
  ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/114)).
* Adds credential store resource for Vault
  ([PR 1](https://github.com/hashicorp/terraform-provider-boundary/pull/114)),
  ([PR 2](https://github.com/hashicorp/terraform-provider-boundary/pull/125)).
* Adds claim scopes attribute to OIDC auth method
  ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/112)).
* Adds account claim maps attribute to OIDC auth method
  ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/111)).

### Bug Fixes

* Make OIDC account attribute for subject ForceNew
  ([Issue](https://github.com/hashicorp/terraform-provider-boundary/issues/119)),
  ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/122)).
* Update static type attribute for host catalog resource
  ([Issue](https://github.com/hashicorp/terraform-provider-boundary/issues/115)),
  ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/121)).

## 1.0.2 (May 06, 2021)

### New and Improved

* Adds OIDC account resource
([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/105)).
* Adds OIDC auth method resource
([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/105)).

### Deprecations/Changes

* Deprecates fields on `resource_auth_method` that will be replaced in the future with generic `attributes` attribute.

## 1.0.1 (February 02, 2021)

### New and Improved

* Adds worker filter to target resource
  ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/76)).

## 1.0.0 (January 20, 2021)

We are bumping the version of the Boundary Terraform provider to v1.0.0 and will release new versions of the provider at its own cadence instead of keeping it in lockstep with Boundary.

### Bug Fixes

* During `terraform apply`, do not update existing user account passwords when the password field is updated in the tf file.
  ([Issue](https://github.com/hashicorp/terraform-provider-boundary/issues/71)),
  ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/70)).

## 0.1.4 (January 14, 2021)

### New and Improved

Update provider to handle new domain errors ([PR](https://github.com/hashicorp/terraform-provider-boundary/pull/63)).

## 0.1.0 (October 14, 2020)

Initial release!
