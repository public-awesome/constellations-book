# get all burns

This will get all burns for both the `sg-721` contracts, it will not include
other contracts like imago contracts. You have to add contracts specifically if
you want others.

```
query Burns($filters: [ContractFilter!], $dataFilters: [DataFilter!]) {
  events(contractFilters: $filters, dataFilters: $dataFilters) {
    edges {
      node {
        contractType
        data
        createdAt
      }
    }
  }
}
```

```
{
  "filters": [
    {
      "contractType": "crates.io:sg-721",
      "events": [
        {
          "name": "wasm",
          "action": "burn"
        }
      ]
    },
    {
      "contractType": "crates.io:sg721-base",
      "events": [
        {
          "name": "wasm",
          "action": "burn"
        }
      ]
    }
  ],
  "dataFilters": []
}
```
