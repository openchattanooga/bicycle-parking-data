# bike-parking-data
WORK IN PROGRESS

## overpass query
```
[out:csv(::type,::lat,::lon,access,bicycle_parking,capacity,covered,fee,'operator:type';true;',')];

// search for the relation named Chattanooga
area
  [place=city]
  ["wikidata"="Q186702"]
  ["name"="Chattanooga"]->.a;


// get all bicycle parking options in the area
(
  nwr["amenity"="bicycle_parking"](area.a);
);

out body center;
```
