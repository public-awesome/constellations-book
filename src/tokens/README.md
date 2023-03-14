# Tokens

## All attributes for all tokens for a given collection

```
query Tokens {
  tokens(
    filterByCollectionAddrs: [
      "stars1g4ucjvrcpwwxrrtmnnrprwkvtnud43294k3mrvtnlpdk2uza7hxseqr58k"
    ]
  ) {
    tokens {
      collectionAddr
      tokenId
      mintedAt
      ownerAddr
      name
      description
      forSale
      imageUrl
      rarityOrder
      rarityScore
      price {
        amount
      }
      priceExpiresAt
      saleType
    }
  }
}
```
