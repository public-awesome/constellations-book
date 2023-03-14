# all events for a given collection

```
query EventsForCollection($data_filters: [DataFilter!]) {
  events(dataFilters: $data_filters) {
    edges {
      node {
        contractType
        eventName
        action
        data
        createdAt
      }
    }
  }
}
```

```
{
  "dataFilters": [
    {
      "name": "collection",
      "value": "stars18d7ver7mmjdt06mz6x0pz09862060kupju75kpka5j0r7huearcsq0gyg0",
      "operator": "EQUAL"
    }
  ]
}
```
