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

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABALICWqAzkcADpJFEIBuyKlAFPY4wGZkAbFPnREAygEEAMgFEx3HmACGKJQDFBwvJVEBtBTxoHDRJEsSjaIKBAECEUFGQhIrxw8yUDclkJVXaAIwIAO4ADmAoAEyUAKzRANYoCQQAXpTMAMx4ABYIABz5BAgEAB5hAFZ4vMxYAOZRAAwAnHhKULFhSAAsAGx1vLx4AOyxWMwo%2BXhYmW4MJowQYfgqEHiiMgCKAKrS7kQAvsYAusaUaygAQgSil1IA8gDCANIA%2BgASMgCSAOLvACqvAAickeCgAlEZ5owEGA6ghqHRoTwkBAwAgoQsYaxUAA5cwIfaMdpOFxEohQPAIFSwiQocnKVT7I7IlmMFkHEAAGhAnjwZCUACN7JQMCBuX5KWQwmhMCADkA)
