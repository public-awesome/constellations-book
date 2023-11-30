# Introduction

**Constellations** is a high-performance and real-time indexer developed by
[Fabien Penso](https://pen.so) originally for
[Stargaze](https://www.stargaze.zone) and now for multiple Cosmos chains.
Constellations is currently used by Stargaze for its main website to display
data in the fastest way possible.

Constellations indexes blocks, transactions, messages and events and is able to
index any Cosmos chain. It also indexes off-chain data like IPFS NFTs to store
width, height, content_type and content_length as well as NFT metadata like
traits and automatically calculate rarity. It also stores Stargaze specific
informations like Stargaze names.

Constellations is:

1. A public facing website available at
   [www.constellations.zone](https://www.constellations.zone).

2. A set of API to fetch data Constellations has indexed. This API is available
	 over GraphQL and self-generated GraphQL documentation is enabled.

You should already know about GraphQL to use Constellations. You can read more
about GraphQL [here](https://graphql.org).

## GraphQL queries

You'll most likely be interested in [transactions](transactions/),
[messages](messages/) and [events](events/).

## Available nodes

As of now, I'm indexing [Stargaze
mainnet](https://www.mainnet.stargaze.constellations.zone/), [Stargaze
testnet](https://www.testnet.stargaze.constellations.zone/), [DYDX
mainnet](https://www.mainnet.dydx.constellations.zone/), [Noble
mainnet](https://www.mainnet.noble.constellations.zone/), and [Neutron
mainnet](https://www.mainnet.neutron.constellations.zone/). This list is
subject to change.

## How is it built?

Constellations is built entirely in Rust, backed with Posgresql and hosted on
bare metal servers for optimum performance. It fetches blocks live from the
blockchain over websockets, and parse them instantly.

It ran fine on a single server, but we wanted to have redundancy to avoid
downtimes. These days it manages way over 10 million requests per day.

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

## Throttling

There is no throttling in place for now but will be soon. Please don't hammer
the server with too many calls.

## Contributing to this documentation

This documentation is available on
[GitHub](https://github.com/public-awesome/constellations-book) and issues and feature requests
can be posted on the [GitHub issue
tracker](https://github.com/public-awesome/constellations-book/issues). Please consider opening a
[pull request](https://github.com/public-awesome/constellations-book/pulls).

## I can't find how to fetch specific data

[Create an issue](https://github.com/public-awesome/constellations-book/issues)
with as many details as possible, contract type, information you want and why
you want to fetch it.

## License

The Constellations documentation are released under
the [Mozilla Public License v2.0](https://www.mozilla.org/MPL/2.0/).
