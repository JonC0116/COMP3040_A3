# Endangered Species in Manitoba
## API description

This is a API which provides information about endangered species within the province of Manitoba. The endangered species that can be returned consists of animals and plants. Users can separate what type of animal they want to see, such as mammals, reptiles, amphibians etc. Furthermore, users can separate the returned animals/plants further by entering the region they can be found in. Additionally, users can separate the animals/plants by severity of their endangerment.

## Endpoint

Our API only has one endpoint, it is the following:

`https://www.gov.mb.ca/nrnd/fish-wildlife/wildlife/ecosystems/index.html`

## Parameters

Our API has four parameters.

| Parameter  | Type    | Required | Description |
| :-------:  | :--:    | :------: | :---------: |
| type       | string  | Yes      | type animal or plants |
| subtype    | string  | Yes      | subcategory of animals or plants|
| severity   | string  | No       | severity of endangerment |
| region     | string  | No       | region animal generally lives in |

- **type**: *One of "Animals" or "Plants"*.
- **subtype**: *One of "Birds", "Mammals", "Reptiles", "Amphibians", "Invertebrates", "Fish" or "Plants"*.
- **severity**: *One of "Endangered", "Threatened", "Extirpated"* .
- **region**: *One of "Central", "Eastern", "Interlake", "Northern", "Parkland", "Pembina", "Western", "Winnipeg"*.

## Sample Request

`https://www.gov.mb.ca/nrnd/fish-wildlife/wildlife/ecosystems/index.html?type="Animals"&subType="Birds"`

`https://www.gov.mb.ca/nrnd/fish-wildlife/wildlife/ecosystems/index.html?type="Plants"&subType="Plants"&region="Northern"`

`https://www.gov.mb.ca/nrnd/fish-wildlife/wildlife/ecosystems/index.html?type="Animals"&subType="Fish"&severity="Endangered"&region="Central"`

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
    "region" : ""
    "nearest_municipality" : "",
    "remaining" : ""
  }
  ...
],
"status" : ""
```

_The array returned by `results` contains all of the animals/plants returned by the API._
_The `...` states that more than one object may be in the array._
