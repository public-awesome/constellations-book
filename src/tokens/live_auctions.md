# tokens listed as live auctions for a given collection

```
query Tokens {
  tokens(filterForSale: "LIVE_AUCTIONS") {
    tokens {
      collectionAddr
      tokenId
      forSale
      saleType
    }
  }
}
```


> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.testnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABACoQDWyAzkcADpJFEoXUAUAZgJYA2K%2BAMQh4AygEMeCdETogAMgEkAagFEA%2BgEEAqgGESCgPIA5WQEpaDJkxaUkNeoytMoEHpKgouEJBrBg8lk7MrEgKYIFOHMLikhFWVBIIJAQADghxAL6BWUg5IAA0IABuYnhcYgBGklQYIA4ZIBlAA)
