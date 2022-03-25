
# Learn solidity by reimplementing solmate specs

Learn solidity by reimplementing these specifications.

Instructions:
- Setup
  - `git clone --recurse-submodules -j8 https://github.com/wassname/solidity-forge-exercises.git`
  - `cd solidity-forge-exercises`
- Learn
  - run `forge test -vvv`
  - see the first error, it's to do with the constructor in erc20
  - find the erc20 file and the FIXME comment (./src/tokens/ERC20.sol)
  - replace fixme with write missing logic untill the first error disappears
  - compare to the [answer](https://github.com/Rari-Capital/solmate/blob/main/src/tokens/ERC20.sol)
  - Repeat
- Now fix the unit tests by going through each FIXME comment in the  file
- repeat for other files
- if you get stuck, cheat by looking at [this](https://github.com/Rari-Capital/solmate/blob/main/src/tokens/ERC20.sol)

This uses [forge](https://onbjerg.github.io/foundry-book/forge/cheatcodes.html), [solmate](https://github.com/Rari-Capital/solmate)'s unit tests.

Reference:
- https://cryptozombies.io/
- https://solidity-by-example.org/
- speedrunethereum.com/

Below is the original readme

-------

# solmate

**Modern**, **opinionated**, and **gas optimized** building blocks for **smart contract development**.

## Contracts

```ml
auth
├─ Auth — "Flexible and updatable auth pattern"
├─ authorities
│  ├─ RolesAuthority — "Role based Authority that supports up to 256 roles"
│  ├─ MultiRolesAuthority — "Flexible and target agnostic role based Authority"
mixins
├─ ERC4626 — "Minimal ERC4626 tokenized Vault implementation"
tokens
├─ WETH — "Minimalist and modern Wrapped Ether implementation"
├─ ERC20 — "Modern and gas efficient ERC20 + EIP-2612 implementation"
├─ ERC721 — "Modern, minimalist, and gas efficient ERC721 implementation"
├─ ERC1155 — "Minimalist and gas efficient standard ERC1155 implementation"
utils
├─ SSTORE2 - "Library for cheaper reads and writes to persistent storage"
├─ CREATE3 — "Deploy to deterministic addresses without an initcode factor"
├─ SafeCastLib - "Safe unsigned integer casting lib that reverts on overflow"
├─ ReentrancyGuard — "Gas optimized reentrancy protection for smart contracts"
├─ FixedPointMathLib — "Arithmetic library with operations for fixed-point numbers"
├─ Bytes32AddressLib — "Library for converting between addresses and bytes32 values"
├─ SafeTransferLib — "Safe ERC20/ETH transfer lib that handles missing return values"
```

## Safety

This is **experimental software** and is provided on an "as is" and "as available" basis.

While each [major release has been audited](audits), these contracts are **not designed with user safety** in mind:

- There are implicit invariants these contracts expect to hold.
- **You can easily shoot yourself in the foot if you're not careful.**
- You should thoroughly read each contract you plan to use top to bottom.

We **do not give any warranties** and **will not be liable for any loss** incurred through any use of this codebase.

## Installation

To install with [**DappTools**](https://github.com/dapphub/dapptools):

```sh
dapp install rari-capital/solmate
```

To install with [**Foundry**](https://github.com/gakonst/foundry):

```sh
forge install rari-capital/solmate
```

To install with [**Hardhat**](https://github.com/nomiclabs/hardhat) or [**Truffle**](https://github.com/trufflesuite/truffle):

```sh
npm install @rari-capital/solmate
```

## Acknowledgements

These contracts were inspired by or directly modified from many sources, primarily:

- [Gnosis](https://github.com/gnosis/gp-v2-contracts)
- [Uniswap](https://github.com/Uniswap/uniswap-lib)
- [Dappsys](https://github.com/dapphub/dappsys)
- [Dappsys V2](https://github.com/dapp-org/dappsys-v2)
- [0xSequence](https://github.com/0xSequence)
- [OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-contracts)
