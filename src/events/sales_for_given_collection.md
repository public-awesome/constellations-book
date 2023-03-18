# sales for a given collection

```
query Mints {
  events(
    filter: SALES
    dataFilters: [
      {
        name: "collection"
        value: "stars1ewpdt2s5t2ktkyzsv3rhe88yeyxpjrfvqg209rac5pn46gffr75qvt8rq3"
        operator: EQUAL
      }
    ]
    sortBy: BLOCK_HEIGHT_DESC
  ) {
    edges {
      node {
        eventName
        action
        createdAt
        data
      }
    }
  }
}
```
