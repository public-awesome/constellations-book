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
