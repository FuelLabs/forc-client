# forc-client

Forc plugin for interacting with a Fuel node.


Note: You will probably require the accompanying [`forc-wallet`](https://github.com/FuelLabs/forc-wallet) plugin in order to sign your transactions:

```sh
cargo install forc-wallet
```

## Examples

While using `forc-deploy` or `forc-run` to interact with a node you need to pass the endpoints with `--url`:

### Localhost

```sh
forc deploy --url localhost:4000 --unsigned
```

### Testnet

```sh
forc deploy --url https://node-beta-1.fuel.network/graphql:443
```

Since deploying and running projects on the testnet cost gas, you will need coins to pay for them. You can get some using the [testnet faucet](https://faucet-beta-1.fuel.network/).

Also the default value of the "gas price" parameter is 0 for both `forc-deploy` and `forc-run`. Without changing it you will get an error complaining about gas price being too low. While using testnet you can pass `--gas-price 1` to overcome this issue. So a complete command for deploying to the testnet would look like:

```sh
forc deploy --url https://node-beta-1.fuel.network/graphql:443 --gas-price 1
```

## License

Apache License, Version 2.0, ([LICENSE](./LICENSE) or <https://www.apache.org/licenses/LICENSE-2.0>)
