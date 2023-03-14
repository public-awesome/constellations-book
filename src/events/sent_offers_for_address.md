# all offers sent for a given address

```
query SentOffersForGivenAddress {
  events(
    filter: SENT_NAME_OFFERS
    forAddresses: ["stars10l56qdud5g6qt3pzywy65urm9cle0mx7aur6zd"]
  ) {
    edges {
      node {
        contractType
        eventName
        action
        data
        createdAt
        blockHeight
        isValid
        expired
      }
    }
  }
}
```
