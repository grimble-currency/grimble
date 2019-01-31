# Grimble API Documentation

This document contains the documentation for the 3 Grimble REST APIs. These endpoints can be grouped in two categories.

## Node API

This endpoint is used to query a node about various information on the blockchain, networks and peers. By default, this REST API will listen on `localhost:4413`. This API is started as the same time as the Grimble node.

This endpoint requires, by default, [Basic Authentication](https://en.wikipedia.org/wiki/Basic_access_authentication). The username is `grimble` and the password can be found in the `.api_secret` file.
To learn about what specific calls can be made read the [node API doc](node_api.md).

## Wallet APIs

### Foreign Wallet API

The foreign API is an endpoint mainly designed to receiving grimbles through a network. This REST API can be started with the `grimble wallet listen` command and by default will listen on `localhost:4415`.

To learn about what specific calls can be made read the [wallet foreign API doc](wallet_foreign_api.md).

### Wallet Owner API

The wallet owner API is an endpoint to manage the user wallet: broadcast transaction, sign transaction, see the current balance... This REST API can be started with the `grimble wallet owner_api` command and will listen on `localhost:4420`. This endpoint must **never** be exposed to the outside world.

This endpoint requires, by default, Basic Authentication. The username is `grimble` and the password can be found in the `.api_secret` file.

To learn about what specific calls can be made read the [wallet owner API doc](wallet_owner_api.md).
