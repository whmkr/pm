# git flow for smart contract development(upgradeable)

### master(main)

`master` branch should include
- smart contract proxy addresses
- smart contract proxy template addresses

when `release` branch was merged to `master`, ci/cd tool should
- update smart contract proxy template to latest template address

`release` -> `master` pr merge can only be done by approved bots
- bot can be some event subscription bot that checks proxy template updates

### release/*

when merged to `release/*` branch, ci/cd tool should
- deploy contracts updated on merge commit
- change template address for deployed contracts


Other branch rule follows same rule as default git flow
