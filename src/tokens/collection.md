# tokens for a given collection

```
query Tokens {
  tokens(filterByCollectionAddrs: ["stars1g4ucjvrcpwwxrrtmnnrprwkvtnud43294k3mrvtnlpdk2uza7hxseqr58k"]) {
    tokens {
      collectionAddr
      tokenId
      name
    }
  }
}
```
