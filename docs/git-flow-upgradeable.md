# git flow for smart contract development(upgradeable)

### master(main)
`master` branch should only allow push from approved bot and admin

`master` branch should include
- smart contract proxy addresses
- smart contract proxy template addresses

when `release` branch was merged to `master`, ci/cd tool should
- update smart contract proxy template to latest template address

`release` -> `master` pr request should automatically queue tx on wallet service(ex. gnosis) when there is one

`release` -> `master` pr merge can only be done by approved bots
- bot can be some event subscription bot that checks proxy template updates

### release/*

when merged to `release/*` branch, ci/cd tool should
- if contract was not previously deployed before, it should
  - deploy upgradeable proxy contract to network
  - add proxy address and template address for new contract
- deploy contracts updated on merge commit
- verify the contract on etherscan using `hardhat-etherscan`
- change template address for deployed contracts
- add transaction hash of the template being deployed

Other branch rule follows same rule as default git flow
