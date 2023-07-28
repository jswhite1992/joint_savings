# joint_savings

This project is a Solidity smart contract that automates the creation of joint savings accounts. The contract accepts two user addresses that can control the joint savings account. The smart contract uses Ethereum's ether management functions to implement various requirements from the financial institution to provide the features of a joint savings account.

## Setup

1. This project requires a local blockchain development environment. Use the JavaScript VM provided by the Remix IDE.

2. After writing the `JointSavings` smart contract, deploy it to the local blockchain.

3. Interact with the deployed smart contract to transfer and withdraw funds.

## Contract Details

The smart contract, named `JointSavings`, includes the following features:

- Two variables of type `address payable` named `accountOne` and `accountTwo`, which store the addresses of the account holders.
  
- A variable of type `address public` named `lastToWithdraw`, which keeps track of the last account to perform a withdrawal.

- Two variables of type `uint public` named `lastWithdrawAmount` and `contractBalance`, which store the value of the last withdrawal and the current contract balance, respectively.

The contract includes the following functions:

- A `withdraw` function that allows the account holders to withdraw a specified amount of Ether. The function includes safeguards to ensure that only the account holders can perform withdrawals and that the requested withdrawal amount does not exceed the contract balance.

- A `deposit` function that allows anyone to deposit Ether into the contract. The contract balance is updated with each deposit.

- A `setAccounts` function that allows the account holders to be changed.

- A fallback function that allows the contract to accept and store Ether sent outside the deposit function.

## Usage

To use the contract, the account holders should first be set using the `setAccounts` function. After this, Ether can be deposited into the contract using the `deposit` function. The account holders can perform withdrawals using the `withdraw` function.

