---
layout: "opentelekomcloud"
page_title: "OpenTelekomCloud: opentelekomcloud_nat_gateway_v2"
sidebar_current: "docs-opentelekomcloud-resource-nat-gateway-v2"
description: |-
  Manages a V2 nat gateway resource within OpenTelekomCloud Nat.
---

# opentelekomcloud\_nat\_gateway_v2

Manages a V2 nat gateway resource within OpenTelekomCloud Nat

## Example Usage

```hcl
resource "opentelekomcloud_nat_gateway_v2" "nat_1" {
  name   = "Terraform"
  description = "test for terraform2"
  spec = "3"
  router_id = "2c1fe4bd-ebad-44ca-ae9d-e94e63847b75"
  internal_network_id = "dc8632e2-d9ff-41b1-aa0c-d455557314a0"
}
```

## Argument Reference

The following arguments are supported:

* `name` - (Required) The name of the nat gateway.

* `description` - (Optional) The description of the nat gateway.

* `spec` - (Required) The specification of the nat gateway, valid values are "1",
    "2", "3", "4".

* `tenant_id` - (Optional) The target tenant ID in which to allocate the nat
    gateway. Changing this creates a new nat gateway.

* `router_id` - (Required) ID of the router this nat gateway belongs to. Changing
    this creates a new nat gateway.

* `internal_network_id` - (Required) ID of the network this nat gateway connects to.
    Changing this creates a new nat gateway.

## Attributes Reference

The following attributes are exported:

* `name` - See Argument Reference above.
* `description` - See Argument Reference above.
* `spec` - See Argument Reference above.
* `tenant_id` - See Argument Reference above.
* `router_id` - See Argument Reference above.
* `internal_network_id` - See Argument Reference above.
