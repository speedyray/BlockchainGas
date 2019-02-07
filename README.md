# Understanding Gas on the Ethereum blockchain
A blockchain is a globally shared, transactional database.
The Ethereum virtual machine -(EVM) is an isolated and sandboxed runtime environment.
Every Transaction which is a message sent from one account to another account on the Ethereum network costs gas.

# Why the Ethereum blockchain needs gas?
The Ethereum virtual machine is a computationally universal machine, a Turing complete machine that is limited by the amount of gas
required to run any instruction.This means that infinite loops that can potentially result in
denial of service attacks by hackers are not possible due to gas requirements.Soon the loops run out of gas or fuel.
The purpose of charging gas for transactions is to limit the amount of work that is needed
to execute the transaction and to pay for this execution at the same time.


# Gas
A unit of transactional cost on the blockchain. In other words the crypto fuel required to perform transaction on 
Ethereum blockchain

# Gas price: 
The gas price field represents the amount of Wei required to execute a transaction.
Wei is the smallest denomination of ether on Ethereum blockchain
It is a value representing how much Ether the user is willing to pay per gas.
Transaction cost can be estimated using the following formula:

` Total cost = gasUsed * gasPrice `


 # Gas Costs
 Transactional operations on the Ethereum blockchain is done by following the bytecode or opcodes.
 
 Opcodes or bytecodes are instructions for the EVM.Each opcode costs a certain amount of gas.
 
 A good list of available opcodes can be found on the [Ethereum Yellow paper](https://ethereum.github.io/yellowpaper/paper.pdf)
 
 See chart below:

![OPCODES](./gcode.png)

 
The different gas requirements can be found on [page 26 in the Ethereum Yellow paper](https://ethereum.github.io/yellowpaper/paper.pdf)

 see Chart below
 
![Gas Cost](./gas.png)


# Advice for Ethereum Blockchain developers in Solidity 
As blockchain developer, it is advisable to be aware of the gas costs of transactions when writing smart contracts.
As much as possible contract developers must try and avoid loops unless they know how much gas it consumes at all times.

# Gas Charges
Gas is charged under these scenarios and circumstances on the blockchain
* Storage or an Increase in the usage of memory
* When computations are performed on operations
* When there is a message call or contract creation  

![CGas Charges](./gastable)

## Technologies
* pragma solidity  - version >=0.4.0 <0.6.0;

## Setup
Tested written code directly on remix.ethereum.org

## Code Examples
Declare a state variable of type address that is publicly accessible



Map an address to unint values

 `mapping (address => uint) public balances;`
     
  Constructor will fire when this contract is created
  Set inventor as creater of this contract:
  
  ` constructor() public {
     inventor = msg.sender;
   }`

## Status
Project is: _finished_

## Inspiration
Credits to Solidity documentation

## Contact
Created by [Raynold](https://ca.linkedin.com/in/raynold-gyasi-036631119) - Email:speedyray2ray@gmail.com Feel free to contact me!



