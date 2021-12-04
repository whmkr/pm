# Dev environment for smart contract development

## hardhat

tldr; industry standard dev environment

### pros
- writes test with javascript/typescript
- rich plugins
- easy to use

### cons
- slower than [foundry](#foundry)
- context switching for writing tests

### plugins

- solidity-coverage
- hardhat-deploy
- hardhat-storage-layout
- hardhat-log-remover
- hardhat-gas-reporter
- hardhat-contract-sizer
- hardhat-abi-exporter

### links

[whmkr-hardhat](https://github.com/whmkr/whmkr-hardhat)
[whmkr-hardhat-utils](https://github.com/whmkr/whmkr-harhat-utils)

## foundry

tldr; not suitable for full test/dev environment (for now)

### pros
- written in rust
- test with solidity
- (probably) super fast
- built in features like [cast](https://github.com/gakonst/foundry/blob/master/cast)

### cons
- written in rust
- lack of plugins

### links

[whmkr-foundry](https://github.com/whmkr/whmkr-foundry)
