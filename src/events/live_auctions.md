# List of tokens current as live auctions

```
query ValidLiveAuctions {
  events(
    contractFilters: [
      {
        contractType: "crates.io:stargaze-reserve-auction"
        events: [{ name: "wasm-create-auction", action: null }]
      }
    ]
    dataFilters: [
      {
        name: "seller"
        value: "stars1rpnqgfdr79zv7zn6d8y888u7vqvpgtr5cqdnuw"
        operator: EQUAL
      }
    ]
    isValid: true
  ) {
    edges {
      node {
        data
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.testnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAKIBuyKAzkcADpJFEIWpUAUDTTUEqeAQygoAYgEsANinxV0RANpduTeo2Xde-ISgAqBAA4I5dEFEHSqAOjER0VFALwBzAQC8EAWjwIq%2BCh4EYYRskEyV1ZlZqOXlgIiQBRGMQAHcBKjgPMwQBaQCglBCTABoibRC5JBgJCSIAXwBdcO465qa1JjBcgXEpGRjmlUHuBKSiE18a-DCO9TIBCVxk%2B0cqAEY8fSQsJwAzMDwAdgBOVzJD1yQANjAADgJbx5hDsiwyfScUPABWKCwwKopGYRJgQQzmCB4OQkACKAFUAIIAGWGrVm7WUYioADUFmIwHIvrglABKWjNBBgJw%2BcmzJhICBgBC0kFELoOVHNNFMNF1EDFEDzPBiAQAIwkPgwIFUfLqQA)
