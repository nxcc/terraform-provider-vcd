---
layout: "vcd"
page_title: "VMware Cloud Director: vcd_nsxt_alb_cloud"
sidebar_current: "docs-vcd-datasource-nsxt-alb-cloud"
description: |-
  Provides a data source to read ALB Clouds for Providers. An NSX-T Cloud is a service provider-level construct
  that consists of an NSX-T Manager and an NSX-T Data Center transport zone.
---

# vcd\_nsxt\_alb\_cloud

Supported in provider *v3.4+* and VCD 10.2+ with NSX-T and ALB.

Provides a data source to manage ALB Clouds for Providers. An NSX-T Cloud is a service provider-level construct that
consists of an NSX-T Manager and an NSX-T Data Center transport zone.

~> Only `System Administrator` can use this data source.

~> VCD 10.3.0 has a caching bug which prevents listing importable clouds immediately (retrieved using
[`vcd_nsxt_alb_importable_cloud`](/providers/vmware/vcd/latest/docs/data-sources/nsxt_alb_importable_cloud)) after ALB
Controller is created. This data should be available 15 minutes after the Controller is created.

## Example Usage

```hcl
data "vcd_nsxt_alb_cloud" "first" {
  name = "cloud-one"
}
```

## Argument Reference

The following arguments are supported:

* `name` - (Required)  - Name of ALB Cloud

## Attribute Reference

All the arguments and attributes defined in
[`vcd_nsxt_alb_cloud`](/providers/vmware/vcd/latest/docs/resources/nsxt_alb_cloud) resource are available.