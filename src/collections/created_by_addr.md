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
