# token bids

```
query Bids($filters: [ContractFilter!], $dataFilters: [DataFilter!]) {
  events(contractFilters: $filters, dataFilters: $dataFilters) {
    edges {
      node {
        data
      }
    }
  }
}
```

```
{
  "filters": [
    {
      "contractType": "crates.io:sg-marketplace",
      "events": [
        {
          "name": "wasm-set-bid",
          "action": null
        }
      ]
    }
  ],
  "dataFilters": []
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAEICWYAzgBQAkAZmQDYr6XpEDaAwhKngEMoKAGLNWeAIQBdADRFaYASgFiWbDpwAiy1ePwyAlEWAAdJESIIAbshQ0ofFIOFqJ7BY3V5K8pSrcNBX89b0pjMwtLKzAAcwRKE3No6KQIMAQkqJTLEOScgF98yyKo0oKQWRBrATwyAQAjJgSMEEjLUxAvd07NYqycok7HfiEUABUCAAcEXqGQKEFWSgA6Mgh0SliAWjhagGsEFCmmIVnK-o6QGztKOc5L6PbB6M6kAUQ5zoB3AUo4baUI7bBoUTqyR4pTpjdZIOZIGBMJiQoilQbSfpoohyfKdEKBHz3DFICpVSiLMhTNCYEAFIA)
