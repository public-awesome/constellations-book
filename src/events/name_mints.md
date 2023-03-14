# name mints

```
query NameMints {
  events(
    contractFilters: [
      {
        contractType: "crates.io:name-minter"
        events: [{ name: "wasm-mint-and-list", action: null }]
      }
    ]
  ) {
    edges {
      node {
        data
        createdAt
      }
    }
  }
}
```
