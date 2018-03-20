## Preamble

    MIP: <to be assigned>
    Title: Create another type asset that can be minted again after creation
    Author: Vorapoap Lohwongwatana, vorapoap@gmail.com
    Type: Standard Track
    Category (*only required for Standard Track): Core
    Status: Draft
    Created: 2018-03-20


## Simple Summary
To connect blockchain to real world usage through Dapp, new token will be needed to be re-minted (or burned) according to a special events

## Abstract
In real world usage, people will go to register their assets through Oracle or Dapp. After some criteria is met, Oracle will mint a new token using the same symbol for the existing asset type. 

Although this can be done on application layer, but you will lose the convenient of using different wallet provided by third-party. And when taking into consideration of the future world where several assets get tokenized. A user will need to have many wallets for each business on Metaverse Blockchain. This doesn't sound practical.


## Motivation
Taking Digix Global [https://digix.global/] where the _Mint Smart Contract_ mint a new DGX token after receiving the signed Ownership Card by all three parties ("Vendor", "Custodian", and "Auditor"). The DGX token will be able to move around the world through different wallet app. At the end, the DGX can be burned in exchange back to real goal by sending to _Recast Smart Contract_.

On Metaverse Blockchain, all of this must be handled by:
1. All token must be created at maximum number and probably held by the Oracle
2. The Oracle sends (issue) new tokens by just sending equal amount tokens representing the deposited gold to such user.
3. The token goes through different wallet and users
4. The final users send token back to Oracle to withdraw the equal amount of real gold.

For the basic functionalities like this look fine, but please consider several fall back:
1. The circulating token in the market doesn't really represent the total gold available in the vault, user need to use special app designed just for this token to find out. This is not natural.
2. If the token held by Oracle get leaked by any reasons, the whole market will be in frustrated state. People will try to withdraw goal more than it is available in the vault.

Consider the similar business case, but now you have several deposit and withdrawal points where user can deposit and withdraw token to and from different Oracles. In this ecosystem, all goal tokens are minted at maximum universe capacity (saying 1,000,000,000 gold tokens) which can virtually represent 1 mega ton of gold. But this time, the gold token only has value only if the sent transaction is attached with special encrypted message given by an oracle. This message is only understandable by special wallet. Users can send token around using this special wallet but once the token are sent using third-party wallet (e.g. Lightwallet). The gold token become invalid because the special attached message is loss. 

In both cases, the problem can be solved easily if token can be re-minted and burned by the oracle at will.



## Specification
On asset creation, user is given an option to create future-mintable asset or standard asset. The maximum supply is no longer needed to be supply for this future-mintable asset type.

To be further discussed


## Rationale
Metaverse Blockchain just needs another type of asset that can be minted or burned at will

## Backwards Compatibility
To be discussed

## Test Cases
To be discussed

## Implementation
To be discussed

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).


