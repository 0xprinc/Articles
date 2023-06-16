Also read it [here](https://mirror.xyz/0x5D4046683516826f2e83a92bF53E1982904D9cd7/lue2o48yuC_kQiRxLcv4HGBxd770-jlxlbrwF7rXELM)  on mirror.xyz


# Tokenisation in Smart Contracts

Tokenisation in a smart contract is basically another representation of some quantity of our interest in the quantifiable way.

The very common example of this is the representation of the liquidity provided by a LP in AAVE as aTokens. Instead of storing the number in the contract itself they tokenised it.

Another common example is the tokenisation of governance in a protocol on the basis of the number of tokens every account have.

The default case is non-tokenisation and hence representing the quantity as just a number. This includes all the quantities we store as state variables and through other means. For example: mapping that stores the counter of number of transactions done by a user, uint totalSupply

# Is tokenisation better?

The answer depends on the use case. 

In my experience as a web3 De-Fi geek, I have observed various advantages of verification of an account through some other ways rather than storing it in the contract storage and its a very common practice. 

This originates the idea of tokenisation as, 

rather than storing each and every contributor or liquidity provider in as a mapping or an array we just give them tokens. Hence we can verify the account later if the account is having the tokens we gave them earlier.

But this idea don’t work in all the cases as there are some situations when storing the value is more profitable than tokenising them as there are only a very few or even a single address linked so to store just that address we can not make another token with a very few or a single total supply.

# When to tokenise

### 1. Reduction of transaction made to single contract

Tokenisation helps in changing the count of token without interacting to the main contract over and over which can lead to the smoother workflow of the protocol. 

reduction of gas fees and time for the user. The reason for this is ??

### 2. Divisibility and transfer of position

Tokenisation also quantises the quantity we are tokenising. This also gives the token holder to transfer some of the tokens to another user to divide the position.

### 3. Security

Using some very useful tokenisation ways to tokenise(ERC20, ERC721 tokens) can be more secure and tamperproof than our implementation of storing the values.

### 4. Enhance Liquidity of the protocol

Tokenisation can also help enhance the liquidity of a protocol. By allowing users to trade tokens, it creates a market for them, which can in turn attract more liquidity to the protocol. This can be seen in the case of AAVE where aTokens(there native token) is used to repay the loan and hence can also be used to increase the liquidity of the pool.

# Where to not tokenise

### 1. Don’t want new contracts

We don’t have to make a new contract for the token. As making another contract only for storing something very stable value and only related to a very few accounts is not feasible.

### 2. Sometimes gas efficient

Tokenisation may not be the best choice when the quantity being tokenised is very small or there are only a few accounts involved. In such cases, storing the value directly may be more efficient and cost-effective.

### 3. Weird constraints

when there are constraints(very less freedom) on the quantity that are very specific to the protocol. For example, only changed by someone with specific ROLE, can’t be divided.

# Ways of tokenisation

There are different ways to apply tokenisation in smart contracts. Some of them are:

### 1. Fungible Tokens

ERC20 is a standard for fungible tokens on Ethereum. It defines a set of rules that Ethereum tokens must follow. This will allow the users to divide, transfer their position and enhance the pool liquidity. 

### 2. Non-Fungible Tokens

ERC721 is a standard for non-fungible tokens on Ethereum. Unlike ERC20 tokens, each ERC721 token is unique and cannot be exchanged for another token. This will make the position of the user transparent, even though indivisible but very personalised for a person. Use case can be when there are so many ROLES in a protocol and there can be more roles to be made in future.

### 3. Native Tokens

Some protocols have their own native tokens that are used to represent different things within the protocol. For example, AAVE has aTokens which represent the liquidity provided by a LP. Native tokens are a good way to tokenise and simultaneously impose the restrictions related to the protocol.

# Conclusion

While coding a smart contract one of the very important aspect is tokenization so we have to choose wisely according to the use case of various quantities to tokenize them or not.
