## Preamble

```
MIP: 3
Title: Digital Assets Secondary Issue (Secondary offering)
Author: Hao Chen
Type: Standard Track
Category: ECO
Status: Draft
Created: 2018-03-29
```

## Simple Summary
To provide asset secondary issue functions for Metaverse Smart Token (MST), not including ETP. 

## Abstract
Digital Assets Secondary Issue（DASI）could be compared to secondary offering tools in the field of securities. 

## Motivation
Under lots of user cases, it is apparent that users can't determine the upper issuance limit of MST. Thus, single issuance has a higher opportunity cost. 

For example, the total number of the first MST issuance is 1 billion which can't meet the market demand and it is hoped to issue another half biliion tokens. In order to lower the opportunity cost, we propose Secondary Issue function. 

## Specification
There are preconditions for DASI. Firstly, assets creation should be based on MIP-004 asset creation function, and the necessary conditions for assets issuance need to be spedified when the asset is created. 

If the following two conditions are satisfied, the asset could be secondarily issued. 
1. One has the right of issuance. Asset issuance rights are defined in MIP-004 and could be transferred to others. 
2. Target asset holdings of the account equals or exceeds the minimum required threshold;

All network consensus verification is required, which involves the change of consensus agreement.

## Rationale
TODO...

## Backwards Compatibility
New function, no need of compatiblity requirment.

## Test Cases
1. Repeated addtional issuance
2. Secondary issue non-existent assets
3. Conduct secondary issuance when users have no issuance right
4. Conduct secondary issuance when the asset holding is lower than minimum required threshold

## Implementation
It is recomended to add secondaryissue（additionalissue）API.
Currently, there is no product-benchmarkeing in the market.
