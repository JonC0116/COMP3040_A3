# Endangered Species in Manitoba
## API description

This is an API which provides information about endangered species within the province of Manitoba. The endagered species that can be returned consists of animals and plants. Users can seperate what type of animal they want to see, such as mammals, reptiles, amhpibians etc. Furthermore, users can seperate the returned animal further by entering the area they can be found in. Additionally, users can seperate the animals by severity of their endangerment.

## Endpoint

Our API only has one endpoint, it is the following:
`https://api.gov.mb.ca/nrnd/fish-wildlife`

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
## Sample Request


## Sample Response
