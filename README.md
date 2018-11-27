# API Guidelines

This repository contains the API design guidelines for Dutch government APIs. The `components` folder contains compliant reusable OpenAPI components which can be included in OpenAPI Specifications (OAS).

## Referring to components

We recommend to use [jsDelivr](https://www.jsdelivr.com/network/infographic) when referring to the resuable OAS components in this repository. For example, if you want to refer to the `Content-Crs` header in `parameters.yaml`, you should use the following URL:

`https://cdn.jsdelivr.net/gh/geonovum/kp-api-guidelines@1.0.0/components/parameters.yaml#/contentCrs`

Example OAS syntax:

```yaml
paths:
  /addresses:
    get:
      parameters:
        - $ref: 'https://cdn.jsdelivr.net/gh/geonovum/kp-api-guidelines@1.0.0/components/parameters.yaml#/contentCrs'
```

## Versioning

Please note that `1.0.0` points to the specific `1.0.0` release of the API Guidelines. Version ranges are also supported, but not recommended:

- `/kp-api-guidelines@1.0/`: latest patch release in the `1.0.x` range, e.g. `1.0.3`
- `/kp-api-guidelines@1/`: latest minor release in the `1.x.x` range, e.g. `1.2.1`.