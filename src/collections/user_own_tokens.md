# list collections where an addr owns at least one token

```
query Collections {
  collections(tokenOwnerAddr: "stars1mtu407haz7g9s4hazdh8mtw94x3v52uaj8xx8c") {
    collections {
      name
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAMIQA25CUKAlhEgM5HAA6SRRUFVN9TAChQQA1sgDyAdyT4AgmDB50RViEYoAhnkYBGOChgAWAAwB2ABYaAXqYDmATkaHLVsOYAc%2ByfcMAPAMwAbgCsAEwwGgBW7r6%2B7lCqAJQs7Jyc3JTUdAzMbBxpnEgaiKlpAL6lFUhlIAA0IIFatBoARlSMGCB1alB4tAAOaJggZUA)
