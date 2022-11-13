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

#### Function declaration