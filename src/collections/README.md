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

## Available sorting

- TOKENS_COUNT_ASC: Sort by the smallest amount of tokens
- TOKENS_COUNT_DESC: Sort by the highest amounf of tokens
- MINTED_AT_ASC: Sort by the least recent minted collection time
- MINTED_AT_DESC: Sort by the most recent minted collection time
- VOLUME_24H_DESC: Sort by the past 24H sales volumes
- VOLUME_7D_DESC: Sort by the past 7 days sales volumes
