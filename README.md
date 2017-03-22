# GuideMe REST API
Project developed using Node.js to implement a basic 
**REST API** for supporting the development of a distributed
Android application named GuideMe App.

## API signatures
The API contains the following entry points:

- ```POST /poi```
  - Adds a new POI (Point Of Interest) to the system, through a JSON object
- ```GET /poi```
  - Obtains all the POI on the system
- ```GET /poi/:id```
  - Obtains information about a particular POI represented by a specific ID
- ```GET /poi/range/:latt/:logt/:distance``` 
  - Obtains information about all the POIs that are in the range of a specific distance from a given coordinates pair
- ```GET /poi/range/:latt/:logt/:distance/:type``` 
  - Obtains information about all the POIs of a given type that are in the range of a specific distance from a given coordinates pair

## POI JSON object
The JSON object that represents the POIs has the following structure:
```
{
  name: name,
  address: address,
  latt: latitude,
  logt: longitude,
  description: description,
  image: imageURL,
  type: POItype
}
```

**name** a string representing the name of the POI

**address** a string containing the address of the POI

**latt** a double with the latitude part of the POI geolocation

**logt** a double with the longitude part of the POI geolocation

**description** a string with a small description of the POI

**image** a string with the image URL of this POI

**type** an integer that indicates the POI type