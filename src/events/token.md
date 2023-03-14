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
