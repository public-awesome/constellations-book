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
