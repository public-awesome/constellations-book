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
