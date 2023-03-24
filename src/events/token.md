# all events for a given token

```
query EventsForTokenId {
  events(
    filter: TOKEN_METADATAS
    forToken: {
      collectionAddr: "stars1ery3ph276meayswezstaulm4vekzz9u825ppf8gx6cxjteplvrrqt33m8k"
      tokenId: "127"
    }
  ) {
    edges {
      node {
        contractType
        eventName
        action
        data
        createdAt
        blockHeight
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAKIBuyKAzgGIR4AqEA1sgJJhHAA6SRRCCqioAKXv34AzAJYAbFPnREGAeQDSJAHIB9ALIkGAQQAihowGVxEyfSaskSnnwn8oEWbIRQU0iEkNgYHhK3CBUKACGeFQAjPgEAMwADgAWAEwA7ABsiBEEVADuCABe4REwsnAALBTMxcUAnDAAHGkArElJks0A5gAeWVB9AFYKSbJkeHhYKAkJcM3MoVYuKCzsYCEgMZnLzvwAvlYAlFwrAmA9CFRn%2BxJIEGAIty4ubqh4Ed4MBEkI5y5BJRNBFEACJF8fH5wfwwBFIjCiFA8Ah4QgwIYUIiAEayaDMAASCGkPRSWLuh3OR2c1IOIAANCAyFFpBFcdcMCAGWFkdIkmhMCADkA)
