# JSON Schema Store

The following changes were made to the original TILT schema, since the very strict linter did not allow the following items:

## Replace 8601 strings
```
created
modified
planned date of change 

changed from
pattern: ^([\\+-]?\\d{4}(?!\\d{2}\\b))((-?)((0[1-9]|1[0-2])(\\3([12]\\d|0[1-9]|3[01]))?|W([0-4]\\d|5[0-2])(-?[1-7])?|(00[1-9]|0[1-9]\\d|[12]\\d{2}|3([0-5]\\d|6[1-6])))([T\\s]((([01]\\d|2[0-3])((:?)[0-5]\\d)?|24\\:?00)([\\.,]\\d+(?!:))?)?(\\17[0-5]\\d([\\.,]\\d+)?)?([zZ]|([\\+-])([01]\\d|2[0-3]):?([0-5]\\d)?)?)?)?$
to
format: date-time
```

## Delete additionalItems
```
deleted all 20 occurences of 
"additionalItems": true,
```

## Example plannedDateofChange
```
changed to
"plannedDateOfChange": "2020-09-20T12:00:00.000000",
```


---


# JSON Schema Store

The largest collection of independent JSON schemas in the world

[![Build status](https://github.com/SchemaStore/schemastore/workflows/Node.js%20CI/badge.svg)](https://github.com/SchemaStore/schemastore/actions)

The repository is meant as a universal JSON schema store, where schemas for popular JSON documents can be found.

Website: [schemastore.org](https://www.schemastore.org/json/)

## Contribute

Contributions are more than welcome. Both to the website itself or to the various schema files. Before contributing, please carefully read the [guidelines](./CONTRIBUTING.md).
