# GOST Query Options

## Selection

Select certain properties of entity in order to reduce the response size

```
$ curl http://localhost:8080/v1.0/Things(5)?$select=name,description
```

## ordering

Order on property

```
$ curl http://localhost:8080/v1.0/Things?$orderby=Name asc
```

## Expand

Expand sub-entities

```
$ curl http://localhost:8080/v1.0/Things(5)?$expand=Locations,HistoricalLocations
```

Select thing with id 5 and expand the corresponding locations and datastreams with observations

```
$ curl http://localhost:8080/v1.0/Things(5)?$expand=Locations,Datastreams/Observations
```

## Pagination

return top 2 of things

```
$ curl http://localhost:8080//v1.0/Things?$top=2
```

Skip the first 3 things

```
$ curl http://localhost:8080/v1.0/Things?$skip=3
```

return 5 observations skipping the latest 10

```
$ curl http://localhost:8080/v1.0/Observations?$top=5&$skip=10
```

Return results with/without count

```
$ curl http://localhost:8080/v1.0/Things?$count=true
```

For the various filter options see <a href="gost_filtering.md">gost_filtering</a>.





