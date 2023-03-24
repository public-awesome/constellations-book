# list collections created by a given address

```
query Collections {
  collections(creatorAddr: "stars1err5c2tc8ha6qa42tpvedgk585dpj35576ny29") {
    collections {
      name
      mintedAt
      createdByAddr
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAMIQA25CUKAlhEgM5HAA6SRRUFVN9TACih4EAQxQQ8AQTBg86IqxCMUovIwCM%2BPAFYoAJhRQAHAAtRANiyiALIYAOANwRgA5gGsdxnWHsArAGYdHQB2CyQCfQBOJQBKFnZOTm5KajoGZjYOJM4kUUREnKI4WlQXKRRCnOExFBcAIQIZOSqiAF9CjqQukAAaEEc1WlEAIypGDBA%2B5WFaezRMEDagA)
