# Endangered Species in Manitoba
## API description

This is a API which provides information about endangered species within the province of Manitoba. The endangered species that can be returned consists of animals and plants. Users can separate what type of animal they want to see, such as mammals, reptiles, amphibians etc. Furthermore, users can separate the returned animal further by entering the area they can be found in. Additionally, users can separate the animals by severity of their endangerment.

## Endpoint

Our API only has one endpoint, it is the following:

`https://api.gov.mb.ca/nrnd/fish-wildlife`

## Parameters

Our API has four parameters.

| Parameter  | Type    | Required | Description |
| :-------:  | :--:    | :------: | :---------: |
| type       | string  | Yes      | type of species |
| subtype    | string  | Yes      | subcategory of animals or subcategory of plants|
| severity   | string  | No       | severity of endangerment |
| region     | string  | No       | region animal generally lives in |

- **type**: *Either "Animals" or "Plants".*
- **subtype**: *Such as "Mammals", "Reptiles", "Amphibians", "Invertebrates", "Fish", "Flowers", "Trees", etc...*
- **severity**: *One of "Endangered", "Threatened", "Extirpated".*
- **region**: *One of "Central", "Eastern", "Interlake", "Northern", "Parkland", "Pembina", "Western", "Winnipeg".*

## Sample Request


## Sample Response



## Resources
The following is the JSON file that will be returned when using the API:

```
"results": [
  {
    "id" : "",
    "name" : "",
    "scientific_name" : "",
    "type" : "",
    "subtype" : "",
    "region" : "",
    "nearest_municipality" : "",
    "remaining" : "",
    "severity" : ""
  }
  ...
],
"status" : ""
```

_The array returned by `results` contains all of the animals/plants returned by the API._
_The `...` states that more than one object may be in the array._
