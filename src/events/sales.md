# all sales

```
query Sales {
  events(
    filter: SALES
    sortBy: BLOCK_HEIGHT_DESC
  ) {
    edges {
      node {
        eventName
        action
        createdAt
        data
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAMoCGANggM5HAA6SRRCAbsitQBQBmAlhRT50pAIIAZAKIkANEWoQ8KAEIERy8QHkAwgGkA%2BgAlJASQDihgCr6AItO0BKOo2bMEYAOY1nTV8yQQYAg%2Bfn5QeAhkQmCiKC6hzGBRZPEJAEYU0ADWhgh8HgAWcb5%2BAL6pROW%2BVVUgMiCsZHh8ZBk0GCB1INThfAAOaJggpUA)
