# all names sorted by offer

```
query Names {
  names(sortBy: OFFERS_DESC) {
    limit
    offset
    total
    names {
      highestOffer
      highestOfferEvent {
        data
      }
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
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAHICGiAzkcADpJFFIUKUAUlEeKAQgekQDyAMWEBRAEoBlAPoARMVIDCAShr1GjADYBLODpQbNEAGYnKCQw00oIKMlqONmVddc1EAFjoDmn1iiCZvhOmt5%2BAUEm%2BGIAbsgobh4eYGT2oYwAvhlMLDn6qAhgAIJWyURQEKh4ZFAoxWBgeDkQAO5I%2BA1NOWSUnFA6aUVdze6aeAiVeGDUdGMeE1Ng5Ig5jItcYABqDrhrRPF4OiY6RTnZYxdZ9JkgADQgsWRHZABGWqwYIPcglFBHAAc0JgQJkgA)
