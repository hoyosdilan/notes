# Solidity

#### Solidity Version
This is the way how you make Solidity use an specific version.

    pragma solidity >=0.5.0 <0.6.0;


#### Contract
En otros lenguajes se llama funcion:

    contract Example {
        ...
    }

#### Types

How can you create a variable?

    uint myUnsingnedInnteger = 100;

#####types:
- **uint**: its value must be non-negative number, is an alias of uint256, 256 bits
- **uint256**: 256 bits
- **uint8**: 8 bits
- **uint16**: 16 bits
- **uint32**: 32 bits
- **string**: UTF-8

####Constants:
It can saves gas cost.

    address public constant MY_ADDRESS = 0x777788889999AaAAbBbbCcccddDdeeeEfFFfCcCc;

####Immutable:

Inmutable variables are like constants. Values of immutable variables can be set inside the constructor but cannot be modified afterwards:

    address public immutable MY_ADDRESS;
    uint public immutable MY_UINT;

    constructor(uint _myUint) {
        MY_ADDRESS = msg.sender;
        MY_UINT = _myUint;
    }

####Math

Basic Operators:
- Addition: +
- Substraction: -
- Multiplication: *
- Division: /
- Modulus: %
- Exponential: **


#### Structs

More complex data types:

    struct Person {
        uint age;
        string name;
    }

#### Array

There are 2 types of array:

##### Fixed:

You can fixed an array to have an specific length:

    uint[2] array;

##### Dynamic:

You can continue adding information to it.

    struct Person {
        uint age;
        string name;
    }

    Person[] people;

##### Access to an array:

You can specify what is the access to an array:

    Person[] public people;

This means that Solidity will create a getter method for it.

#### Types of variables:

- Local:
  - Declared inside a function.
  - Nor stored on the blockchain.

- State:
  - Declared outside a function.
  - Stored on the blockchain.

- Global:
  - Provides informaiton about the blockchain e.g. msg.sender.

#### Ether and Wei

Similar to how one dollar is equal to 100 cent, one ether is equal to 1018 wei.

    // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.17;

    contract EtherUnits {
        uint public oneWei = 1 wei;
        // 1 wei is equal to 1
        bool public isOneWei = 1 wei == 1;

        uint public oneEther = 1 ether;
        // 1 ether is equal to 10^18 wei
        bool public isOneEther = 1 ether == 1e18;
    }

#### Gas
How is calculated?
- Gas spent: is the total amount of gas used in a transaction.
- Gas price: is how much ether you are willing to pay per gas.

Gas limit
- Gas Limit: you set it, max amount of gas you're willing to use.
- block gas limit: max amount of gas allowed in a block, set by the network.


#### If/else

it is the same as it's in Js, also there is the ternary operator.


#### Function declaration


??? https://solidity-by-example.org/state-variables/
