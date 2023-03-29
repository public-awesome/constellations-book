# sales for a given collection

```
query Sales {
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

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAMoCGANggM5HAA6SRRCAbsitQBSPPMBmASwop86UgEEAMgFESvPmDIoyAMWGi81cQG0FfOvoNEkZROPogoEClSgpBEJJaMHWlXBZDUVWgIwIAO4ADmAoAEzUAKwRANYosQQAXtSsAMx4ABYIABw5BAgEAB7BAFZ4-KxYAObhAAwAnHhkUFHBSAAsAGzV-Px4AOxRWKwoOXhYaS5MxswQwfjKEHjiMgCKAKrSrkQAvkYAukbUyygAQgTiZ1IA8gDCANIA%2BgASMgCSAOIvACpPACJyO4KACUhhmzAQYGqNHBsyQEDACDhsxY7FQADkzAgdswWg4nLiiFA8AhlFCJCgiUoVDt9hC9gp6bsQAAaEDuPCCMgAIyo1AwIDZ3hJgmCaEwIF2QA)
