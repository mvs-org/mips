## Preamble

```
MIP: 4
Title: Digital Assets - Issuance Right and the Extensions of Other Rights 
Author: Hao Chen
Type: Standard Track
Category: ECO
Status: Draft
Created: 2018-04-10
```

## Simple Summary
To provide Metaverse Smart Token (MST) with transferrable issuance right. 

## Abstract
The issuance right refers to the right to conduct initial issuance and secondary issuance, and is defined at underlying technology of blockchian as a part of Metaverse MST infrastructure. 

## Motivation
The transferability is a necessary feature of Digital Asset. 

## Specification
The distribution of rights and obligations

By default, the first issuer will have the issuance right and is only owned by him.

At the time of first issuance, the issuer could specify the minimum issuance threshold percentage for asset holdings.

The definable range of the threshold:
-1           No threshold requirement. That is, if one gets the issuance right, he can conduct additional issuance without limitation of times.
0            Never be able to conduct additional issuance. Even if one has the issuance right, he cannot use it.
1~100    Asset holdings accounting for the percentage of issued shares. The amount of asset holdings for the account with issuance rights must exceed the threshold percentage.


Each asset has only one issuance right which can be transferred separately and the asset holdings will not be affected. After the transfer, the original issuer no longer has the right of secondary issuance, while the receiving account gets it. 

## Rationale

To be written.

## Test Cases

To be written.

## Implementation
add new type `asset certificate` in output attachment;

