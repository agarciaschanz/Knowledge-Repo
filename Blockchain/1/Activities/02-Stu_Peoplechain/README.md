# Peoplechain

The best way to understand how the blockchain keeps track of transactions is to emulate one!

As a class, you will be emulating  the activities of a fictitious blockchain that are involved in confirming a transaction (notice that the operational details of blockchains might differ from this example, say if 'proof of stake' is used instead of 'proof of work' for instance). 

## Instructions

You are going to proceed in 4 steps for this exercise:

* Step 1: Share your fictitious account balance in the slack channel 'Balance', by slacking out a message, like so: 10 BTC. All the members in the network will know that this is your balance since you sent the message (similar to a digital signature)

* Step 2: Everyone will take on the role of a Bitcoin user, and slack out one single transaction in the 'Broadcasted Transactions' channel, like so: 

    ```python
    { to: "StudentA", from: "StudentB", amount: "$100", fee: "$1.00" }
    ```
    Note: You are not required to post valid transactions. For instance, you could send more BTC than you have, or have the transaction send BTC to you from someone else. We will identify the valid transactions in the next step.

* Step 3: We will now assume the role of nodes in the network that validate transactions. Mark transactions that you have validated with a thumbs up symbol in slack. A transaction is valid if the 'from' section matches the sender of the message in slack (similar to a digital signature) and the amount sent is not larger than that person's balance. Your instructor will assign one student to copy the transactions that have received a 'thumbs up' from at least half of the classroom over to the 'MemPool channel'. The Memory Pool contains validated transactions waiting to be confirmed.


* Step 4: During the final stage, students will assume the role of miners. For this step, your instructor will pick a random number between 1 and 10 and you will enter your guesses in the 'class activities' channel. Whoever guesses the correct number first gets to pick 5 transactions and adds them to the next block and receives 1 BTC and the sum of all transaction fees of the transactions added to the pool. Here, a block consists of 1 slack message that looks like this (for the first block, the Previous Block's Hash should be zero, after that, it should increase in increments of 1):

    ```python
    Previous Block's Hash
    { to: "StudentA", from: "StudentK", amount: "$100", fee: "$1.00" }
    { to: "StudentC", from: "StudentD", amount: "$75", fee: "$1.50" }
    { to: "StudentF", from: "StudentN", amount: "$99", fee: "$2.00" }
    { to: "StudentG", from: "StudentE", amount: "$65", fee: "$1.20" }
    { to: "StudentL", from: "StudentA", amount: "$12", fee: "$3.00" }
    This Block's Hash
    ```
Repeat the final stage until all transactions from the MemPool are added to the chain.



---

© 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
