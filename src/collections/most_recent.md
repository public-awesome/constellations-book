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
