# all events for a given collection

```
query EventsForCollection($data_filters: [DataFilter!]) {
  events(dataFilters: $data_filters) {
    edges {
      node {
        contractType
        eventName
        action
        data
        createdAt
      }
    }
  }
}
```

```
{
  "dataFilters": [
    {
      "name": "collection",
      "value": "stars18d7ver7mmjdt06mz6x0pz09862060kupju75kpka5j0r7huearcsq0gyg0",
      "operator": "EQUAL"
    }
  ]
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAKIBuyKAzgGIR4DCEANswlCgJYRIAUAJGACGKIQH0AZp2Yp8VdEQDaAERFCa02XgCEAXQCURYAB0kRIggqoqvYaI0y5CwWsma5hk2fMWwAcwQqI1MfHyQIMARg71DzKB4UPCEOABUCAAcEENjzS0oAOSFEbJzkrh4S2LshStCoPAQRBDAAQRRaogBfSu7vXs6QABoQMiE8TiEAIzYqDBAvc2NwNQctKiWFRUqF2KWkIqyMIiX41nZypCXBjqXR5lwN45AqUTwqAEYADjAAdgo8H5wOAAKzAKAADAA2OAAL0hAA9wekYeCAJyfSEAJih4IA1jB0sCYD8AKy49K4oQk4HggEAC1wYygVCw4L8BD84KuNxAEEySRQ9EeSxIAEUAKotAAySx62V0pgGwyo9U46TQmBAnSAA)
