# Messages

Messages contains all blockchain messages

For example, the following gets all `/cosmos.staking.v1beta1.MsgDelegate`
messages including its transaction hash and block height.

```
query Messages {
  messages(typeUrls: ["/cosmos.staking.v1beta1.MsgDelegate"]) {
    edges {
      node {
        typeUrl
        data
        blockHeight
        transaction {
          hash
        }
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABALIIDO5AhgOYVHAA6SRRiltFAFCgQA4IAqngA25dEQDajEAHooEcnEUA6ciioBrAJZIaKgG4BGAEYINRlSXI0AIghEIaVFAhkBdAJQNmrVgjA6ch8WP1YkCDAEELCw3gFhEV9Y1jAXKmSUkxFoTQAJBG0aAAsUTNiUPCokaigUbQgWJlCU1mKqcmLysIBfbqI%2BloHkwZ6QHqA)

Or get all cosmwasm related messages for two cosmwasm methods:

```
query Message {
  messages(
    typeUrls: ["/cosmwasm.wasm.v1.MsgExecuteContract"]
    cosmwasmMethods: ["swap_nfts_for_tokens", "approve_all"]
  ) {
    edges {
      node {
        typeUrl
        data
        blockHeight
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABALIIDO5AhgOYJHAA6SRRiltFAFM66ygQAOCAKp4ANuXREA2oxAB6KBHJwA7lVUA6DdoBuARi0lyNAKIAPBLBQIAwhFR4qUFPIC6vPstW64ZFAALCDApWXlyDUEAfSQAMxRyaLiIPGiUCABrZHJ5ABoieSpBQTwIPQRoqnFxDy8ASgYvVgQwOnImlj5WJBD6Ji7u-iFRCWahsCoUKnHugCNxaEyACQQASxpAt0G%2BAF9x-a7D3ZBdoA)
