# Getting Started

## Get Emerald

**Emerald**

Download Emerald at [https://github.com/ETCDEVTeam/emerald](https://github.com/ETCDEVTeam/emerald)

```text
$ git clone https://github.com/ETCDEVTeam/emerald.git
```

Within the working directory run

```text
$ npm link
```

This process may take a few minutes. When it's done, run `emerald -h` to see Emerald commands.

```text
$ emerald -h

   emerald 0.0.1 

   USAGE

     emerald <command> [options]

   COMMANDS

     new                 Create a new project               
     wallet              Boot Emerald Wallet                
     explorer            Boot Explorer                      
     testrpc             Run testnet for ethereum classic   
     deploy              Deploy solidity to network         
     help <command>      Display help for a specific command

   GLOBAL OPTIONS

     -h, --help         Display help                                      
     -V, --version      Display version                                   
     --no-color         Disable colors                                    
     --quiet            Quiet mode - only displays warn and error messages
     -v, --verbose      Verbose mode - will also output debug messages
```

