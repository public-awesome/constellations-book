# Collections

Query
```graphql
query Collections($limit: Int, $sortBy: CollectionSortBy, $offset: Int, $tokenOwnerAddr: String, $creatorAddr: String) {
  collections(limit: $limit, sortBy: $sortBy, offset: $offset, tokenOwnerAddr: $tokenOwnerAddr, creatorAddr: $creatorAddr) {
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
    limit
    offset
    total
  }
}
```

Variables
```json
{
  "limit": 2,
  "sortBy": null,
  "offset": null,
  "tokenOwnerAddr": null,
  "creatorAddr": null
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAMIQA25CUKAlhEgM4AUAJObXLSukQJKoANEVaMIeFACECvMpWp0GAZXFSCw1hABmWxgh78hIlBADWyAPIB3JPgCCYMHl5KUeWkgDmGqHgQBDEzwHJxc3D08ASiJgAB0kIiIoCioaeiZmDi4Ddk5uYTEJaV5RVWlhbV19Esq9FGETcyRrW2DHZ2MzSxt7duFfAKCQjtYBwPFh6LiExKSUhXTGGPjZ2c5-TwQV1aIwBEZfWgAHRSRt1cbkRjIYVHPZqwQAI0ZuLZnVsZQEMDsUe8SyXkaQYwwBRCQ-kQ4K4qB%2Bf3uAF97lluPdavp7iYUP5yNtkUhESBBCAAG7%2Bdz%2BJ5URgYEDTRKxECo-4YIgAJkE2yZhTUTN4SBglC5MyZGNZAqF5BFjJAl2aPTaTn5EKlMqITK%2BE3aKsFlHiRJJB3cJzpIERQA)

## Available sorting

- TOKENS_COUNT_ASC: Sort by the smallest amount of tokens
- TOKENS_COUNT_DESC: Sort by the highest amounf of tokens
- MINTED_AT_ASC: Sort by the least recent minted collection time
- MINTED_AT_DESC: Sort by the most recent minted collection time
- VOLUME_24H_DESC: Sort by the past 24H sales volumes
- VOLUME_7D_DESC: Sort by the past 7 days sales volumes
