# Movement Testnet Coins

This a package for bootstrapping multiple coins at once for testing purposes.

## Dependency
Aptos CLI

## How to use

1. Initialize your aptos account

```shell
$ aptos init
```
you will get a ".aptos" folder in your current folder.
```shell
config.yaml
profiles:
  default:
    private_key: "0x0000000000000000000000000000000000000000000000000000000000000000"
    public_key: "0x0000000000000000000000000000000000000000000000000000000000000000"
    account: "0x1234"   # your_original_account
    rest_url: "https://fullnode.devnet.aptoslabs.com/v1"
    faucet_url: "https://faucet.devnet.aptoslabs.com/"
```
2. Get test MOVE
```shell
$ aptos account fund-with-faucet --account your_original_account --amount 100000000
```

3. Compile code
```shell
$ aptos move compile
```
4. Publish package
```shell
$ aptos move publish
```