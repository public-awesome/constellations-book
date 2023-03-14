# get all collections

GraphQL will have all internal attribute documentation.

```
query Collections {
  collections {
    collections {
      name
      mintedAt
    }
  }
}
```

```
curl 'https://api.mainnet.stargaze.constellations.zone/graphql' \
	-H 'Accept-Encoding: gzip, deflate, br' \
	-H 'Content-Type: application/json' \
	-H 'Accept: application/json' \
	-H 'Connection: keep-alive' \
	--compressed \
	--data-binary '{"query":"query Collections { collections { collections { name mintedAt } } }"}'
```

