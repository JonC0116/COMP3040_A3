# Endangered Species in Manitoba
## API description

This is a API inerface which provides the information about endangered species within the province of Manitoba. Users can get information about the name, type and area in which they mostly existed.


## Endpoint
- https://api.gov.mb.ca/nrnd/fish-wildlife


## Parameters
- type(string): Type of animals. One of "Birds", "Mammals", "Reptiles", "Amphibians", "Invertebrates", "Fish". Required.
- severity(string): Severity of endangerment. One of "Endangered", "Threatened", "Extirpated". Optional.
- Area (string): Area animal generally lives in. One of "North", "South", "East", "West". Optional.


## Resources
{
  "results":
  {
    "id": "",
    "name": "",
    "type" "",
    "area":
    "":
  },
  "status": ""
}


## Sample response


