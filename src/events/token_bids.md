# token bids

```
query Bids($filters: [ContractFilter!], $dataFilters: [DataFilter!]) {
  events(contractFilters: $filters, dataFilters: $dataFilters) {
    edges {
      node {
        data
      }
    }
  }
}
```

```
{
  "filters": [
    {
      "contractType": "crates.io:sg-marketplace",
      "events": [
        {
          "name": "wasm-set-bid",
          "action": null
        }
      ]
    }
  ],
  "dataFilters": []
}
```
