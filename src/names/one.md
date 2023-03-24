# name with its record

```
query Name {
  name(name: "sex") {
    highestOfferEvent {
      data
    }
    highestOffer
    name
    mintedAt
    contractAddr
    ownerAddr
    associatedAddr
    records {
      recordName
      recordValue
      verified
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAHICGiRwAOkkUUhQgBSOLpHUgDOCAHlwCUVWvXoALAJYBzcQm4oA8gDNl%2BAKIA3ZChF0x9MGRRlRYgL5mJMuQpVq8VhkydxJqBGACCKJ1AioeGRQKF5gYI769BAA7kj4YRFOZNzc0JLGnomRBngI-nhg3HoG9HkFYOSITmX5EIUAamQANrg1RNp4ksqSnk6W%2BgPmIAA0IJpkXWQARs3yGCCjPFBdAA5omCDmQA)

```
query Name {
  name(name: "penso") {
    highestOfferEvent {
      data
    }
    highestOffer
    name
    mintedAt
    contractAddr
    ownerAddr
    associatedAddr
    records {
      recordName
      recordValue
      verified
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAHICGiRwAOkkUUhQgBSOLpHUgAOyAzhC4BKKrXr0AFgEsA5hIR8UAeQBmK-AFEAbshSi64%2BmDIoyY8QF9zk2fMWr1eawybO4U1AjABBFM6gQqHhkUCjeYGBOBvQQAO5I%2BOGRzmR8AlBSJl5JUYZ4CAF4YHz6hvT5hWDkiM7lBRBFAGpkADa4tUQ6eFIqUl7OVgaDFiAANCBaZN1kAEYtChggYyB8UN3caJggFkA)
