# token-list

Community managed token list used as default token list by [Fluent Wallet](https://fluentwallet.com/) .

## Who can submit new tokens

Anyone can submit new tokens through pull request.

## Requirements

### Semantic versioning

Lists include a `version` field, which follows [semantic versioning](https://semver.org/).

List versions must follow the rules:

- Increment major version when tokens are removed
- Increment minor version when tokens are added
- Increment patch version when tokens already on the list have minor details changed (name, symbol, logo URL, decimals)

Changing a token address or chain ID is considered both a remove and an add, and should be a major version update.

Note that list versioning is used to improve the user experience, but not for security, i.e. list versions are not meant
to provide protection against malicious updates to a token list; i.e. the list semver is used as a lossy compression
of the diff of list updates. List updates may still be diffed in the client dApp.

### Conflux core space and EVM space token requirements

The submitted token needs to meet below requirements:

1. The token contract has been verified on [ConfluxScan](https://confluxscan.io)
1. The token needs to be in the top 100 on ConfluxScan
1. Has more than 50 token holders.

### Other Ethereum based network

1. Listed on [CoinGecko](https://www.coingecko.com/)

## PR message requirements

Please provide **plain URL** of ConfluxScan or CoinGecko. For example:

👍 plain URL with annotation

```markdown
conflux scan token URL: https://confluxscan.io/token/cfx:acdrf821t59y12b4guyzckyuw2xf1gfpj2ba0x4sj6
conflux scan token holders URL: https://confluxscan.io/token/cfx:acdrf821t59y12b4guyzckyuw2xf1gfpj2ba0x4sj6?tab=holders
```

```markdown
coingecko token URL: https://www.coingecko.com/en/coins/ethereum
```

👎 none plain URL

```markdown
[conflux scan token URL](https://confluxscan.io/token/cfx:acdrf821t59y12b4guyzckyuw2xf1gfpj2ba0x4sj6)
```

## How To Submit PR
* Add the Token Info to the `tokens` property.
* Follow the [Semantic versioning](https://github.com/conflux-fans/token-list#semantic-versioning) to modify the `version`.
* Modify the `timestamp` property.
  
After the PR was accepted, JSDELIVR takes 12 hours and up to 7 days to update the global CDN. 
