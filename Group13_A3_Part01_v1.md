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
| type       | string  | Yes      | type of species |
| subtype    | string  | Yes      | subcategory of animals or subcategory of plants|
| severity   | string  | No       | severity of endangerment |
| region     | string  | No       | region animal generally lives in |

- **type**: *Either "Animal" or "Plant".*
- **subtype**: *Such as "Mammal", "Reptile", "Amphibian", "Invertebrate", "Fish", "Flower", "Tree", etc...*
- **severity**: *One of "Endangered", "Threatened", "Extirpated".*
- **region**: *One of "Central", "Eastern", "Interlake", "Northern", "Parkland", "Pembina", "Western", "Winnipeg".*

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
  },
  ...
],
"status" : ""
```

_The array returned by `results` contains all of the animals/plants returned by the API._

_The `...` states that more than one object may be in the array._

## Sample Requests

`https://www.gov.mb.ca/nrnd/fish-wildlife/wildlife/ecosystems/index.html?type="Animal"&subType="Bird"`

`https://www.gov.mb.ca/nrnd/fish-wildlife/wildlife/ecosystems/index.html?type="Plant"&subType="Flower"&region="Northern"`

`https://www.gov.mb.ca/nrnd/fish-wildlife/wildlife/ecosystems/index.html?type="Animal"&subType="Fish"&severity="Endangered"&region="Central"`

## Sample Responses
The following response would be provided for `https://www.gov.mb.ca/nrnd/fish-wildlife/wildlife/ecosystems/index.html?type="Animal"&subType="Bird"`.
```
"results": [
  {
    "id" : "1",
    "name" : "Baird's Sparrow",
    "scientific_name" : "Ammodramus bairdii",
    "type" : "Animal",
    "subtype" : "Bird",
    "region" : "Central",
    "nearest_municipality" : "Portage La Prarie",
    "remaining" : "600",
    "severity" : "Endangered"
  },
  {
    "id" : "2",
    "name" : "Burrowing Owl",
    "scientific_name" : "Athene cunicularia",
    "type" : "Animal",
    "subtype" : "Bird",
    "region" : "Winnipeg",
    "nearest_municipality" : "Winnipeg",
    "remaining" : "180",
    "severity" : "Endangered"
  },
  {
    "id" : "3",
    "name" : "Ferruginous Hawk",
    "scientific_name" : "Buteo regalis",
    "type" : "Animal",
    "subtype" : "Bird",
    "region" : "Northern",
    "nearest_municipality" : "Churchill",
    "remaining" : "420",
    "severity" : "Endangered"
  },
  ...
],
"status" : "success"
```

The following response would be provided for `https://www.gov.mb.ca/nrnd/fish-wildlife/wildlife/ecosystems/index.html?type="Plant"&subType="Flower"&region="Northern"`.
```
"results": [
  {
    "id" : "1",
    "name" : "Great plains Ladies'-Tresses",
    "scientific_name" : "Spiranthes magnicamporum",
    "type" : "Plant",
    "subtype" : "Flower",
    "region" : "Northern",
    "nearest_municipality" : "Gillam",
    "remaining" : "1249",
    "severity" : "Endangered"
  },
  {
    "id" : "2",
    "name" : "Western Silvery Aster",
    "scientific_name" : "Aster sericeus",
    "type" : "Plant",
    "subtype" : "Flower",
    "region" : "Northern",
    "nearest_municipality" : "Flin Flon",
    "remaining" : "421",
    "severity" : "Threatened"
  },
  {
    "id" : "3",
    "name" : "Hair Prarie-Clover",
    "scientific_name" : "Dalea villosa",
    "type" : "Plant",
    "subtype" : "Flower",
    "region" : "Northern",
    "nearest_municipality" : "Snow Lake",
    "remaining" : "318",
    "severity" : "Threatened"
  },
  ...
],
"status" : "success"
```
