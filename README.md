# FreeGeoDB

Free database of geographic place names and corresponding geospatial data

## Entities

 * airports
 * cities
 * countries (admin-0)
 * lakes
 * ports
 * railroads
 * regions (admin-1)
 * roads
 * time zones

## Formats

 * [CSV](Distribution/CSV/)
 * [JSON](Distribution/JSON/)
 * [MySQL](Distribution/MySQL/)

## Representation of geographic coordinates

All geographic coordinates are stored in the [WKT format](https://en.wikipedia.org/wiki/Well-known_text).

In WKT, the pairs of coordinates are always written as `x y`.

Such tuples, potentially along with other tuples, are then wrapped by one of 18 geometric objects, e.g. `POINT`, `MULTILINESTRING` or `MULTIPOLYGON`.

The most basic example would be `POINT(x y)`.

Accordingly, the order of latitude and longitude in those tuples is always `long lat`, as in `POINT(long lat)`.

## Authoritative data source

The single authoritative source for all data is in [`Source/json`](Source/json).

If you want to make any changes, please apply them in that folder only.

All other data files are generated from the files in that authoritative set.

## Contributing

All contributions are welcome! If you wish to contribute, please create an issue first so that your feature, problem or question can be discussed.

## License

```
Copyright 2015 delight.im <info@delight.im>

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
