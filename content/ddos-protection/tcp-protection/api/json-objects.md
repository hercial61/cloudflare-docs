---
title: JSON objects
pcx_content_type: reference
weight: 3
meta:
  title: Advanced TCP Protection API - JSON objects
---

# JSON objects

This page contains examples of the JSON objects used in the API.

## Prefix

```json
{
  "id": "31c70c65-9f81-4669-94ed-1e1e041e7b06",
  "prefix": "192.0.2.0/24",
  "comment": "Game ranges",
  "excluded": false,
  "created_on": "2022-01-01T13:06:04.721954+01:00",
  "modified_on": "2022-01-01T13:06:04.721954+01:00"
}
```

## Prefix in allowlist

```json
{
  "id": "31c70c65-9f81-4669-94ed-1e1e041e7b06",
  "prefix": "192.0.2.0/24",
  "comment": "Game ranges",
  "enabled": true,
  "created_on": "2021-10-01T13:06:04.721954+01:00",
  "modified_on": "2021-10-01T13:06:04.721954+01:00",
},
```

The `prefix` field can contain an IP address or a CIDR range.

## SYN flood rule or out-of-state TCP rule

```json
{
  "id": "31c70c65-9f81-4669-94ed-1e1e041e7b06",
  "scope": "region",
  "name": "WEUR",
  "rate_sensitivity": "medium",
  "burst_sensitivity": "medium",
  "created_on": "2021-10-01T13:10:38.762503+01:00",
  "modified_on": "2021-10-01T13:10:38.762503+01:00"
}
```

The `scope` field value must be one of `global`, `region`, or `datacenter`. You must provide a region code (or data center code) in the `name` field when specifying a `region` (or `datacenter`) scope.

The `rate_sensitivity` and `burst_sensitivity` field values must be one of `low`, `medium`, or `high`.