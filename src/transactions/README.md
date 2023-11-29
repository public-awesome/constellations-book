# Transactions

Transactions contains all blockchain transactions

For example, the following gets all transactions related to a specific
transaction hash (Note: a hash can happen multiple times, to ensure you get the
right one you have to check the block_height as well).

```
query Transactions {
  transactions (
    hashes: ["000B1766A13ABE292D7CB861E9BA977E3C4E8B73F15A9F7CB01243FBE3963213"]
    sortBy: BLOCK_HEIGHT_DESC
  ) {
    edges {
      node {
        hash
        blockHeight
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABACp4CGSAzuVCgJYTVHAA6SRRKF1tDTVIgAp2nTt0o06jJAAlyVABYIq6IgG1WIAAy6AQgEYA7ADYTAQQMBmc3oCiAJgCcDgCJGAwnoAcJg3ac9cycjIzsrDwAWO289IysAMQMAVmCEzz1tAwdIxPsrJxMrB2stAF1RMSoIPBQ9AjU9ABkAeQ8AaQB9WTsASQBxWRJO1zsAZQ9KgEoWSs4EMABzFVmOMU4kCDAEVfX1xQVFOb2AIwAbaABrWQR6RcUUY84AX2PXtff3kGegA)
