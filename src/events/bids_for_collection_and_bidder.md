# bids for a given collection and given bidder

```
query BidsForGivenBidder {
  events(
    dataFilters: [
      {
        name: "bidder"
        value: "stars1rmxl4fps24pe8s9uv8an3nqpng3ggyf8sfavr0"
        operator: EQUAL
      }
      {
        name: "collection"
        value: "stars19jq6mj84cnt9p7sagjxqf8hxtczwc8wlpuwe4sh62w45aheseues57n420"
        operator: EQUAL
      }
    ]
    contractFilters: [
      {
        contractType: "crates.io:sg-marketplace"
        events: [{ name: "wasm-set-bid", action: null }]
      }
    ]
    sortBy: BLOCK_HEIGHT_DESC
  ) {
    edges {
      node {
        txHash
        action
        contractInfo
        createdAt
        isValid
        eventName
        action
        data
      }
    }
  }
}
```
