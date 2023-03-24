# get all burns

This will get all burns for both the `sg-721` contracts, it will not include
other contracts like imago contracts. You have to add contracts specifically if
you want others.

```
query Burns($filters: [ContractFilter!], $dataFilters: [DataFilter!]) {
  events(contractFilters: $filters, dataFilters: $dataFilters) {
    edges {
      node {
        contractType
        data
        createdAt
      }
    }
  }
}
```

```
{
  "filters": [
    {
      "contractType": "crates.io:sg-721",
      "events": [
        {
          "name": "wasm",
          "action": "burn"
        }
      ]
    },
    {
      "contractType": "crates.io:sg721-base",
      "events": [
        {
          "name": "wasm",
          "action": "burn"
        }
      ]
    }
  ],
  "dataFilters": []
}
```

> [Try it out live on explorer](https://studio.apollographql.com/sandbox/explorer?endpoint=https%3A%2F%2Fconstellations-api.mainnet.stargaze-apis.com%2Fgraphql&explorerURLState=N4IgJg9gxgrgtgUwHYBcQC4QEcYIE4CeABAEIx5IDOAFACQBmAlgDYr6XpEDaAwhKngCGUFADEWbPAEIAugBoitMIJSDxrdpy4ARFWon5ZASiLAAOkiJEEAN2QoaUfiiEj1kjoqYa8lBctV3TUUA-R9KE3NLK2swAHMESlMLGJikCDAEZOjUqycBYRQAFQIABwQU3KtQyqqoPAQVBDAAQRRamIBfDu7o3s6QORAbQTxGQQAjZkSMECirMxBvD0WtDvncxfyXQpLy1aItoTZKADpGCHRKOIBaAHYAJgBGRbkOhZBbe0oDrneYjZVD5IQSIA6LADugkocFe-1Si0KFyQ4JAE3IKJA8KIvSqMh6bxy2SqW2crmKZQqGEOIHqTTOFyucUeTxuE2hVMJJM%2BdlQP2pfyJqUBQMWILB1Mh0Nhg2xHyR-FR6Ioi2xuNy%2BKJ6vklUWoSCvl%2BmoGQ0o9UYpTQmBAnSAA)
