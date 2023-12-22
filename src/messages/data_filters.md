# Filtering messages on attributes

You can filter on anything you see from the `data` field using jsonpath. Please
note the value has to be including the type, for if you want to filter based on
a `String` value use `"\"value\""`, for `Integer` use `"14"`.

```
query MessagesFundRenewalForTokenId {
  messages(
    cosmwasmMethods: ["fund_renewal"]
    attributeFilters: {operator: AND, filters: [{path: ["$.msg.fund_renewal.token_id"], value: "\"allegedly\"", operator: EQUAL}]}
  ) {
    edges {
      node {
        cosmwasmMethod
        data
        blockHeight
        transaction {
          errorMessage
        }
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABALIIDO5AhgOYUBiMSYASsggO5UA29EeAFQgBrZAEkwRYAB0kRIokq0KAClnz5UCOThcdZFAAsIYcuiIBtaSABmTMAH087Lt2sBddRqooUeAJYARjAoCPT%2B3KF4ZlIQAA74PvzmAIIAcgAiADRENhFRMRbAcT6G5lYgACQAdHDkNNV2zE4uPNUoIsgO-mAeOQBuPLjm1jzcCHRg3ATWOfGJHXjmAKIAigCqKQAyAL7uO14AlFJe8ghgdOQnchrySCYI17e3Wjp6cAbGvTfPRGA%2BVFOz0C3GgwgAEgh-DRDCggbc-FQkNQoCh-BA5DIfr8iPg8PwyEo6PCNAdsfIybdKUQyWSQDsgA)
