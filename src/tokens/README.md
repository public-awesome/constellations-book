# Tokens

Tokens contains all NFT tokens. Always use a collection filter or the query
will be slow

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
