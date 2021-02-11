# AS-Tetcore

A collection of resources to develop proof of concept projects for Tetcore in AssemblyScript.
AssemblyScript compiles a strict subset of TypeScript to WebAssembly using Binaryen.

At the moment, this repository is mainly home for a collection of smart contract examples and a small smart contract library to write contracts for [Tetcores contracts pallet](https://github.com/tetcoin/tetcore/tree/master/frame/contracts), but it might be extended with more examples in the future.

## Setup

This repository is using yarn and yarn workspaces. You also need a fairly up-to-date version of node.

### [./packages](packages)

The packages folder contains the PoC libraries and projects.

### [./contracts](contracts)

The contracts folder contains a number of example contracts that make use of the [`as-contracts`](packages/as-contracts) package.
The compiled example contracts in the [contracts folder](contracts) can be deployed and executed on any Tetcore chain that includes the contracts pallet.

## Getting started

1. Clone the whole `as-tetcore` repository.

```
$ git clone https://github.com/tetcoin/as-tetcore.git
```

2. Install all dependencies

```
$ yarn
```

3. Compile all packages, projects and contract examples to wasm

```
$ yarn build
```

To clean up all workspaces in the repository, run:

```
$ yarn clean
```

## Write your own contract

The `@tetcore/as-contracts` and `@tetcore/as-utils` packages are not being published to the npmjs registry. That's why you need to add the complete `as-tetcore` repository as a dependency directly from git.

```
$ yarn add https://github.com/tetcoin/as-tetcore.git

// or

$ npm install https://github.com/tetcoin/as-tetcore.git
```

In your projects, you can then import the as-contracts functions directly from the `node_modules` folder

**The recommended way of writing smart contracts is using the [Rust Smart Contract Language `ink!`](https://github.com/tetcoin/ink).**

Another way of writing Smart Contracts for Tetcore is using the [Solidity to Wasm compiler Solang](https://solang.readthedocs.io/en/latest/running.html#using-solang-with-tetcore).

## Disclaimer

Everything in this repository is highly experimental and should not be used for any professional or financial purposes.

## License

The entire code within this repository is licensed under the [GNU GENERAL PUBLIC LICENSE 3.0](LICENSE). Please [contact us](https://www.tetcoin.org/contact/) if you have questions about the licensing of our products.
