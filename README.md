# bicycle-parking-data
> Bicycle Parking Locations in Chattanooga

## download link
https://raw.githubusercontent.com/openchattanooga/bicycle-parking-data/refs/heads/main/files/bicycle_parking.csv

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

## note
Data comes from OpenStreetMap and is under the Open Database License (ODbL).
