# Introduction

**Constellations** is a high-performance and real-time indexer developed by
[Fabien Penso](https://pen.so) for [Stargaze](https://www.stargaze.zone), a L1
blockchain on Cosmos focusing on NFTs. Constellations is currently used by
Stargaze for its main website to display data in the fastest way possible, and
we decided to make its API available to anyone.

Constellations is:

1. A public facing website available at
	 [www.constellations.zone](https://www.constellations.zone) to view its data
	 This is mostly used to "validate" internal information, and you are invited
	 to use the [Stargaze main website](https://www.stargaze.zone) instead,
	 unless you're looking for information not available there.

2. A set of API to fetch data Constellations has indexed. This API is available
	 over GraphQL and self-generated GraphQL documentation is enabled.

You should already know about GraphQL to use Constellations. You can read more
about GraphQL [here](https://graphql.org).

## How is it built?

Constellations is built entirely in Rust with
[tendermint-rs](https://github.com/informalsystems/tendermint-rs), backed with
Posgresql and hosted on bare metal servers for optimum performance. It fetches
blocks live from the blockchain over websockets, and parse them instantly. It 
currently is running on 3 servers:

1. [Dedibox](https://www.dedibox.fr/): Xeon E3 1245v5, 32GB
2. [Hetzner](https://www.hetzner.com/): AMD Ryzen 3600, 64GB
3. [Interserver](https://my.interserver.net/): AMD RYZEN 5600X, 64GB

It ran fine on a single server, but we wanted to have redundancy to avoid
downtimes.

## Safety

While I try to minimize bugs and issues, Constellations sometimes (but rarily)
stops indexing, or has an indexing issue which means it does not reflect the 
blockchain data. It is *highly* recommended to use Stargaze RPC servers to verify
information if you are moving tokens. For example, if you want to send STARS to
a given Stargaze name, you should use the RPC server to get the STARS address
associated with that given name, and not Constellations which could lead to
sending STARS to an old associated address if the indexer stopped.

## Timestamps

All timestamps you get are UTC and don't include timezone.

## User Agent

Add a way to contact you in the `User-Agent` header in case I need to get in
touch with you if you are making too many requests.

## Contributing to this documentation

This documentation is available on
[GitHub](https://github.com/penso/constellations-book) and issues and feature requests
can be posted on the [GitHub issue
tracker](https://github.com/penso/constellations-book/issues). Please consider opening a
[pull request](https://github.com/penso/constellations-book/pulls).

## License

The Constellations documentation are released under
the [Mozilla Public License v2.0](https://www.mozilla.org/MPL/2.0/).
