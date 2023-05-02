# Connecting to Kovan/Ropsten using the web3.auto method:

`from web3.auto import w3`

Then, the web3.auto will search for an environment variable called WEB3_PROVIDER_URI which we demonstrate in the course in [22.1 here](../1/Activities/06-Stu_Accident_Report_System/Solved)

For example, the `.env` file could look something like:

```WEB3_PROVIDER_URI=https://kovan.infura.io/v3/aa3c1e7b65054c8595581a4241ff7b40
CRYPTOFAX_ADDRESS=0xB58F764B1a68c9ABc581E67427943D82b232EC87
```


Using this method will allow us to maintain the same code while swapping out the environment variable with either their local provider, infura, or other types of providers like websocket and is also the preferred method since it reduces the opportunity for error. [Here's the docs for how the automatic detection works](https://web3py.readthedocs.io/en/stable/providers.html#how-automated-detection-works)


## Troubleshooting
If the contract is working locally, then the ABI is likely not the culprit and indeed points to the networking as the problem. Infura also supports Websockets, and so does web3.auto, so using `wss://kovan.infura.io/ws/v3/aa3c1e7b65054c8595581a4241ff7b40` as the WEB3_PROVIDER_URI may help as well.

### Notes

Since this is deployed to a testnet and not using the local Ganache, we  will also need to manually sign contract transactions using a private key that we can store in the same `.env` file, and use the key to sign as shown [here](https://web3py.readthedocs.io/en/stable/web3.eth.account.html#sign-a-contract-transaction)

Effectively, the steps are now split into:

1. Build the transaction by calling buildTransaction instead of transact against the contract function
2. Sign the transaction with a key with something like w3.eth.account.sign_transaction(unsigned_txn, private_key=private_key)
3. Send the signed transaction to the chain via w3.eth.sendRawTransaction
This is basically the same as we learned in 19.1, where we build a function to create_raw_tx and another to sign and send it [here](../../19-Blockchain-Python/1/Activities/05-Stu_Sending_Txns_Back/Solved/main.py)

The main difference here is calling buildTransaction against the contract function to generate the raw tx instead of just creating one with a dictionary and passing it to the account.sign_transaction function.

