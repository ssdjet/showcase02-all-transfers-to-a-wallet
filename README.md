# Showcase squid 02: all Transfers to a given wallet

This squid captures all `Transfer(address,address,uint256)` events where the receiver is `vitalik.eth`. This includes ERC20, ERC721 transfers and possibly events with the same signature made with other protocols. See more examples of requesting data with squids on the [showcase page](https://docs.subsquid.io/evm-indexing/configuration/showcase) of Subsquid documentation.

Dependencies: Node.js, Docker.

## Quickstart

```bash
# 0. Install @subsquid/cli a.k.a. the sqd command globally
npm i -g @subsquid/cli

# 1. Retrieve the template
sqd init showcase02 -t https://github.com/subsquid-labs/showcase02-all-transfers-to-a-wallet
cd showcase02

# 2. Install dependencies
npm ci

# 3. Start a Postgres database container and detach
sqd up

# 4. Build and start the processor
sqd process

# 5. The command above will block the terminal
#    being busy with fetching the chain data, 
#    transforming and storing it in the target database.
#
#    To start the graphql server open the separate terminal
#    and run
sqd serve
```
A GraphiQL playground will be available at [localhost:4350/graphql](http://localhost:4350/graphql).
