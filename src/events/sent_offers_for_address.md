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

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAMrIoDyAZlfgM4BiEeA4gJYBuyAgmGHgjp0iwADpIiRBF1R0AFOMmSqbADYp86UgFEAcgBUA%2Bru4BZbYYoMG2gEolFSqs179BdQVoDaokHRQAhnh0AIwADKoArABsWGAwYJEA5rEoAMwADgBeBADuBNGRMHhwAJxQqghhcAAeAOwBxdFZYL4Auo4AlCKOkghgSYI9EkqSSBBgCMOjo1AQqHgBUCj6BBkIvTPS5LoBiJujSyhs8wdKYAGBZ5JQApf93CjXRABGqtAA1gASCGxJABZPEYzIhsOgANQCqjYrWBWxqGTYAlhIIAvpt0SNMaiQAAaEAcIJsAJvQQYEB4vy3NgZNCYECooA)
