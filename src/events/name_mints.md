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

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAHICGiAsgJaoDORwAOkkUQgG7Ip0AULbNlAio8ZKCgBi1ADYp8ddEQDaAwW2at1g4aPEoAKgQAOCJUxBQx8ugDpqEdEgoIAtHFry8FtdvZd6JWVgImdEcxAAdzI6OHdPVzIkMFcZajoUCwAaIn0HJCUkGBkZIgBfAF1fQTLqqq0ASkZqhDAAcwQGTT8kCDAEZq0-MDIUMmr1KwRR1oBBTKGa6tqtFbKQLJAOMjxqMgAjGU6MEA2QOitqYzRMEDKgA)
