# Implementing Ether Management Functions (Joint Savings Account)

In this activity, you will begin building a JointSavings account smart contract that allows two addresses to manage a savings account by implementing basic functions for `depositing`, and `withdrawing` ether from a contract's address. 

## Instructions

* Open the Remix IDE and open the starter file.

* Create a new contract named `JointSavings`; it should look something like this:

```solidity
contract JointSavings {
 // insert code here
}
```

* Inside this new contract define a variable named `account_one` of type `address` and set it's value to one of the `wallet's addresses` that you generated from your mnenonic phrase. Then define a second variable named `account_two` of type `address` and set it as another one of your addresses.

* Next, define third variable named `balanceContract` of type _public uint_. This variable will allow us to check the balance of our contract while depositing and withdrawing.


* Now define a function named `withdraw` that will accept a `uint` named `amount`, and a `payable address` named `recipient`.

* Inside the `withdraw` function, you are going to call the `transfer` method on the passed `recipient` variable and tell it the `amount` to transfer. Then, call the `balanceContract` variable and set it equal to the balance of the contract. The inside of the function should look something like this:

```solidity
recipient.transfer(amount);
balanceContract = address(this).balance;
```

* Next implement a `public payable` function named `deposit`. Inside this function, call the `balanceContract` variable and set it equal to the balance of the contract like so: `balanceContract = address(this).balance;`

* Notice that the `deposit` function holds no logic referring to amount deposits. Think back on why this function does not require this logic; it is because we are just trying to move the Ether into the contract's own address.

* Calling the `balanceContract` variable and setting it equal to the contract's balance inside each function allows it to update the balance with each deposit or withdrawal.

* Finally, add the default fallback function that was previously discussed so that our contract can store `Eth` sent from outside the deposit function.

## Challenge

* In future exercises, we will be implementing checks to add additional features. Think about what different `if/then` conditions you could create to add additional features now.

## Hints

* Don't forget that the `withdraw` function needs to be `public`.

* Don't forget that the `deposit` function needs to be `public payable`.

* Don't forget that the address that we are passing into our withdraw function to transfer the funds to must also be marked `payable`.

---

© 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
