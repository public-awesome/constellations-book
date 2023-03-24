# received offers on owned NFT

```
query receivedOffersOnOwnedNfts {
  events(
    filter: RECEIVED_OFFERS_ON_OWNED_NFT
    forAddresses: ["stars15y38ehvexp6275ptmm4jj3qdds379nk07tw95r"]
    isValid: true
  ) {
    edges {
      node {
        eventName
        data
        isValid
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABHglAgJYBuCYA8gGYP4DOdSdA7krQHIMoWRYAB0kRIghqoWACjESJDCgBsU%2BdEQBKAUQDCOgJIA1HQBEA%2BnQBi1nVoDKV3lYDqvcxd7WAKgsUMEHgAgmBgpCwsCCyaANoiICwoAIZ4LACMAKwEAMwAHAgAFjQAHgAOAGwATADsmWUocHAALABWrTlYYSw5NQCcSADWAAw1KJx9mXgJALr%2BEhQsxskqFGCaKHi4-gCUwvOSYADm0fviihJIEGAIZxcXUsgovMmIBxdgySnviovLq2AfgBfA4g85goEgAA0ICoqQoyQARipohgQNDElA8BQGmiQECgA)
