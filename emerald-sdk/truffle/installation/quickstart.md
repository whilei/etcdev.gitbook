# Quickstart

## Truffle Box

Truffle boxes are boilerplates that can be modules, example dapps, front-end libraries, and more. ETCDEV Team has contribute a **starter kit** that comes with everything you need to start using smart contracts from a barebones react app.

## Setup

Create a working directory for your dapp.

```text
$ mkdir starter-kit
$ cd starter-kit
```

## Unbox

Download a Truffle Box 

```text
$ truffle unbox <box_name>
```

Within the working directory you created, unbox the starter kit and allow Truffle to unbox

```text
$ truffle unbox shanejonas/react-box-web3-tod
```

## Compile & Migrate

Within the working directory, compile contract source files, then run migrations to deploy contracts.

```text
$ truffle compile
$ truffle migrate
```

Migrations may return an error 

`$ truffle migrate  
Could not connect to your Ethereum client. Please check that your Ethereum client:  
- is running  
- is accepting RPR connections  
- is accessible over the network  
- is properly configured in your Truffle configuration file (truffle.js)`

This error message mentions the `truffle.js` file contained in the starter-kit that was unboxed. This is truffle's javascript configuration file that needs to be setup properly when migrating the dapp to an Ethereum Client.

## Configure



