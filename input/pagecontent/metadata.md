
#### R3

For R3, the return from ```/metadata?mode=terminology``` is a Parameters resource 
with a series of system parameters (of value uri) with sub-parts for the versions (of type code).

```json
{
  "resourceType": "Parameters",
  "parameter": [
    {
      "name": "system",
      "valueUri": "http://example.com/fhir/CodeSystem/example-code-system-1"
        "parameter": [
            {
              "name": "version",
              "valueCode": "1.0.0"
            }
        ]
    },
    {
      "name": "system",
      "valueUri": "http://example.com/fhir/CodeSystem/example-code-system-2"
        "parameter": [
            {
              "name": "version",
              "valueCode": "20230930"
            }
        ]
    }
  ]
}
```