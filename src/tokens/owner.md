# tokens for a given owner

```
query Tokens {
  tokens(
    ownerAddr: "stars1mtu407haz7g9s4hazdh8mtw94x3v52uaj8xx8c"
  ) {
    tokens {
      collectionAddr
      tokenId
      name
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABACoQDWyAzkcADpJFEoXUAUDTTEA7kvgEEwYPOiJ0QVFAEM8VAIxwUMACwAGAOwALaQC8NAcwCcVFTt1gtADiU8jKgB4BmAG4BWAEwxpAKysOHKygJTiIASlpQphZKJBp6Ri4mKAgAG1SEKBQASwgkIREorhjkAEkwIqYkaUQigF9QhqQ6kAAaEBdZbOkAIwyqDBA2ySg8bIAHNEwQOqA)
