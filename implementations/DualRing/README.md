# DualRing: A Truffle Solidity Project

This project implements the DualRing signature scheme, a ring signature method. In addition to the basic implementation, this project also explores the integration of the DualRing signature with Bulletproof to reduce the signature size.

## Repository Structure

- `contracts/`: Solidity contracts implementing the core functionalities.
- `migrations/`: Truffle migration scripts for deploying contracts to the Ethereum network.
- `test/`: Test cases and scripts for validating the contracts' functionalities.
- `build/`: Contains the compiled contract artifacts.
- `data/`: (Description needed; not provided in the initial information.)
- `truffle-config.js`: Truffle configuration file.

## Contracts

- `DualRing.sol`: Implementation of the DualRing Signature without Bulletproof. It provides the basic functionality of the DualRing signature scheme.
- `DualRingBulletproof.sol`: Enhanced version of the DualRing signature combined with Nisa, aiming to achieve log(n) signature size.
- `nisa.sol`: Implementation of the Bulletproof based SumArguments.
- `alt_bn128.sol`: Contains the ECC precompiled helper functions, essential for elliptic curve operations.

## Migrations

- `1_nisa_migration.js`: Migration script for the `nisa.sol` contract.
- `2_dualring_bulletproof_migration copy.js`: Migration script for the `DualRingBulletproof.sol` contract.
- `3_dualring_basic_migration.js`: Migration script for the `DualRing.sol` contract.

## Tests

- `dualring_bulletproof_test.js`: Test script for the `DualRingBulletproof.sol` contract functionalities.
- `dualring_test.js`: Test script for the basic `DualRing.sol` contract functionalities.
- `nisa_test.js`: Test script for the `nisa.sol` contract functionalities.
- `test_with_external.js`: Test script for Verifying siganture is persistent data.

## Reference 
check the original paper [here](https://eprint.iacr.org/2021/1213.pdf)
