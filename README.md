# Hyperledger Caliper Benchmarks for ERC20 Token transfer

This repository contains sample benchmarks that may be used by Caliper, a blockchain performance benchmark framework. This code is created from Hyperledger Caliper Benchmarks repos.
## Prerequisites

- Install docker
- install docker compose

## Setup
1. Clone the repo
2. Configure `networks/networkconfig.json`.
```
"contractDeployerAddress": "xxxxxxxxxxxxxxxxxx",  // กระเป๋าที่ใช้สร้าง contract 
"fromAddress": "xxxxxxxxxxxxxxxxxx", // กระเป๋าที่ mint เหรียญไปใส่ หรือถ้าจะให้ง่ายใช้กระเป๋าเดียวกับ "contractDeployerAddress"
"erc20": {
  "address": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx",  // wallte address ของ token erc-20 ของเหรียญที่สร้างมา
```
3. Configure `benchmarks/scenario/simple/utils/simple-state.js` edit line 56
``` 
target: "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" // กระเป๋าปลายทางที่จะให้โอนเหรียญ
```
4. change owner dir caliper-benchmarks-erc20
```
chown -R 1000:1000 caliper-benchmarks-erc20
```
5. Run `docker-compose up`

## Ref.
> https://github.com/prasanth0105/caliper-benchmarks-erc20
> https://medium.com/coinmonks/benchmark-blockchain-using-hyperledger-caliper-4c3f7f93896b

