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
