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
