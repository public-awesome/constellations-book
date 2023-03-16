# sales for a given collection

```
query Sales {
  events(
    contractFilters: [
      {
        contractType: "crates.io:sg-marketplace"
        events: [{ name: "wasm-finalize-sale", action: null }]
      }
    ]
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
        createdAt
        data
      }
    }
  }
}
```
