# Endangered Species in Manitoba
## API description

This is a API which provides information about endangered species within the province of Manitoba. The endagered species that can be returned consists of animals and plants. Users can seperate what type of animal they want to see, such as mammals, reptiles, amhpibians etc. Furthermore, users can seperate the returned animal further by entering the area they can be found in. Additionally, users can seperate the animals by severity of their endangerment.


## Endpoint
- Our API only has one endpoint.
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


