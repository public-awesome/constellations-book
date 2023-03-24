# Events

Events contains all blockchain cosmwasm events, mints, airdrops, sales. You
have to know what events you're looking for, or what contract types. Unless
they're very noisy and useless, all cosmwasm events are saved.

If you are publishing a new contract, using events and attributes is the best
way to ensure this will be indexed by Constellations.

For example, the following get all events related to the `pegasus` contract,
order by block height DESC (most recent event first):

```
query Events {
  events(
    contractFilters: [{ contractType: "crates.io:pegasus", events: [] }]
    sortBy: BLOCK_HEIGHT_DESC
  ) {
    edges {
      node {
        eventName
        action
        data
        createdAt
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAKIBuyKAzkcADpJFEIWpUAUDTTUEqeAQygoAYgEsANinxV0RANrAivfkJQAVAgAcEcuiCiDpVAHRiI6HQHMBVGFX0AaZq2pz5AXSIBfD125UEHgoAEIEciEAMgDyAMIA0gD6ABIkAJIA4snqiQAiJADKsf4AlLT%2BTAhgVgg09IzcTEgQYAjlDY2VrgByAogVnWrmSAONYAIoAqPchggTVQCCKNPeA6sN694gjiBkAnhiAgBGErUYINsgVIZiWmiYIN5AA)

Or another example for `badge-hub` contracts:

```
query Events {
  events(
    contractFilters: [{ contractType: "crates.io:badge-hub", events: [] }]
    sortBy: BLOCK_HEIGHT_DESC
  ) {
    edges {
      node {
        eventName
        action
        data
        createdAt
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAKIBuyKAzkcADpJFEIWpUAUDTTUEqeAQygoAYgEsANinxV0RANrAivfkJQAVAgAcEcuiCiDpVAHRiI6AEYCwAcwQBaABYxL%2BgDTNW1OfIC6RAC%2BflzcVBB4KABCBHJRADIA8gDCANIA%2BgASJACSAOKZ6ukAIiQAysmhAJS0oUwIdgg09IzcTEgQYAi1rW313gByAoh1fWrmSKNtYAIoAlPchgizDQCCKAuBo1utO4Eg7iBkAnhiApYSTRggByBUhmJaaJgggUA)

This will show all `wasm-fair-burn` for the `badge-hub` contract:

```
query Events {
  events(
    contractFilters: [
      {
        contractType: "crates.io:badge-hub"
        events: [{ name: "wasm-fair-burn" }]
      }
    ]
    sortBy: BLOCK_HEIGHT_DESC
  ) {
    edges {
      node {
        eventName
        action
        data
        createdAt
      }
    }
  }
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAKIBuyKAzkcADpJFEIWpUAUDTTUEqeAQygoAYgEsANinxV0RANpduTeo2Xde-ISgAqBAA4I5dEFEHSqAOjER0AIwFgA5ggC0ACxh2TS9c1bUcvLAREgCiMYgAO4CVHCuAGYCYniudjB4SCZEAL4Aur7cOYUFakxUEHgoAEIEctUAMgDyAMIA0gD6ABIkAJIA4l06HQAiJADKLUoAlLSFCM4INKp%2BSBBgCHNl6iyUAHLhCIXK2jZZ28pgAigCxxp4CNcLAIIod8XbH0wfOSAANCAyAI8GIBHYJEsMCB-iAqGYxPo0JgQDkgA)
