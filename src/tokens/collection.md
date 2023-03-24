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

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABACoQDWyAzkcADpJFEoXUAUAZgJYA2K%2BAIQIBhCDx4IoKLhCQBBMGDxV0RANp0QVFAENlARgDmAFhhQAVgDc8UAA4B3ewA88eFHCRI8tvPfKWUJBgwYwBmACYATmNyULg8AKQeWzBycJgALx0AdgALJyoELDwAVgAOck0AXQBKWgYmJhZKJBp6RkamKDEJKRl5RTwGzuZWJABJMGHOpB1EaaIAX2HlpEWQABoQSz0uHQAjCSoMEE2tKDwuWzRMEEWgA)
