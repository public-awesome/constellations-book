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

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABACoQDWyAzkcADpJFEoXUAUDTTAZgJYA2KfACECAYQj9%2BCKCl4QkAQTBg8VdEQDanLkzogqKAIZqAjAHMALDCgArAG54oABwDurgB548KOEiR4zniu5PYoSDBglgDMAEwAnJbk0XB4YUj8zmDksTAAXkYA7AAWHlQIWHgArAAc5Po6TAC6OgCUtI3MrEg09Iy6RFCS0rLySip4nUwslEgAkmBTRHC8qAhgiihLEK5I%2BMqqS0hGiEtgCFRQeLzOcgpL3BB4AMpG0ku8cEbmCACqePwlngTLwUAQAPJ4c6Tfq6YHXMHPIZ4BBLIK8KAIDqwgYnCAwVBLAC%2BaOumIAoh5nLwUVRNksqG8ECQCM5UTiSf1OUSQAAaED2EFGABG0ioGBAfIMVxuaEwICJQA)
