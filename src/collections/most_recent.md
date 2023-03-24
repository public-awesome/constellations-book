# get most recent minted collections

Query
```graphql
query Collections($collectionsLimit: Int, $sortBy: CollectionSortBy) {
  collections(limit: $collectionsLimit, sortBy: $sortBy) {
    collections {
      image
      description
      tokensCount
      website
      createdAt
      collectionAddr
      name
      mintedAt
    }
  }
}
```

Variables
```
{
  "collectionsLimit": 2,
  "sortBy": "MINTED_AT_DESC"
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAMIQA25CUKAlhEgM4AUAJFBVTfUwDK1xaKdEQCSqADRFWjCHhQAhAiLKVqdBgGU5iggEoiwADpIiRDmu4MW5AUJHtO6no36CUU2fKUOvug8amZuZOVkyGJsHBAgCGAOYIkVFEYAiMUHi0AA4aSElRKBAA1siMZDCo%2BcEA7ggARoxCiUFRGQgxKAhgAIIoVWYWXLndYGB4-URIMYgTgqhdvVUAvkkrSEsgEiAAbjGZMXVUjBgggWZGIIPO1m5CFyIATBJJF35K90QXALKiAHIAKgBRAAiAH1uv9QcDAZoSBcTBstulMjkTiAlkA)
