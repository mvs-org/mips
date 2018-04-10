## Preamble

```
MIP: 2
Title: Adjust reward rate of deposit function
Author: Chen Hao
Type: Standard Track
Category: Core/ECO
Status: Draft
Created: 2018-01-24
```

## Simple Summary
Because of deposit function for, users can get more ETP bonus from MVS ecosystem, which is bad inflation.
Need to change inflation rate by adjusting reward rate. If Metaverse use the current reward rate, there are few problems:
* The inflation rate is a little bit high
* If large amount ETP deposit expire, they may have an impact on ETP price

Refers to current reward rate:
![etprate](https://user-images.githubusercontent.com/15893135/33869224-9582fadc-df42-11e7-88d5-9a7997d1134c.png)

Refers to [issue 1](https://github.com/mvs-org/mips/issues/1).

## Specification
Fix a relative lower bonus rewards each block.

### ETP Total Amount and its Distribution
ETP Total Amount and its Distribution

| Holders |  Amount | 
| --------------------------------- | ----------------- | 
| Initial Holdings of Foundation |   25,000,000             |  
| ICO Investors    |   25,000,000             | 
| Mining and Coinbase Rewards |   30,000,000             |  
| Interest Rewards for Deposit   |  20,000,000            | 

We can query this API to query the total interest rewards generated in real time. Presently, the coinlock interest reward we have designed is always greater than 1. As such, if we consider the deposit function in isolation, it is an inflationary mechanism with the maximum annualized income being 20%. 
In other words, we will inevitably exceed the 100 million ## Analysis Process
The following are calculations are predominantly based on estimates because the results will be referenced in other sections. 

### Analysis Process
The following are calculations are predominantly based on estimates because the results will be referenced in other sections. 

According to our data, deposits have followed a roughly U-shaped distribution. 1-year deposits make up the majority, with middle-duration deposits being the least common. We will assume that the average yield of deposits across the entire network is 13%. 

Based on previous statistics, over 10 million ETP have been deposited at some point of time, reference [API 1](https://explorer.mvs.org/api/depositsum). At the moment, interest rewards across the entire network total about 1.44 million ETP, reference [API 2](https://explorer.mvs.org/api/rewards). From these figures, we can calculate that the observed average yield of deposits across the entire network is 14.19%, which is in line with our estimations. 

10 million ETP makes up about 17.94% of the circulating supply, hence we assume that 17.94% of each year’s circulating supply will be deposited. ETP cap at some point in time in the future. 

bout 1 million new blocks will be generated each year, which means that 2.85 million ETP will be added to the circulating supply in a linear fashion. Taking into account the availability of ETP, we take half the ETP mined = 1.425 million ETP.
Hence, we estimate that an additional 1.425m * 17.94% = 250,000 ETP will be deposited each year on top of the baseline amount, **and further estimate that it will take about 14 years for the total supply of ETP to reach 100 million** . 
Even if deposits across the entire network double to 35.88%, **it would require over 7 years for the total supply of ETP to reach 100 million**. We conclude that with no change in the consensus mechanism, the total supply of ETP will exceed 100 million in **2032**. In the extreme case, we will reach 100 million in **2025**.  
Thus, we have sufficient time to adjust the deposit function.


### Solution
Suppose that use the same decay model as found in the mining reward mechanism. 
Assumptions:  
1.  The amount decays once every N blocks. Let the number of decayals be n. 
2.  Let the decay factor be m.
3.  Let the current total interest be s.
4.  Each block generates a fixed amount of ETP b. 
Then we have:
![image](https://camo.githubusercontent.com/60a78ca46d34376fbd5d6efe359619b7f7d8142c/68747470733a2f2f6c617465782e636f6465636f67732e636f6d2f6769662e6c617465783f5c6c696d5f7b6e5c72696768746172726f772b5c696e6674797d2673706163653b5c73756d5f305e6e7b6d5e6e7d2a4e2a622673706163653b3d2673706163653b32303030303030302673706163653b2d2673706163653b73)

introduce the attenuation coefficient 0.95 and the attenuation height interval 500,000, assuming the total interest is 1.5 million when the main network activates MIP002:
Let the decay factor = 0.95 and N = 500,000. Assuming that the current total interest s = 1.5 million when MIP 002 is activated, we have:
![image](https://camo.githubusercontent.com/f0e4b52bef5b6f9aafdbe967be1b7ac643fd72dc/68747470733a2f2f6c617465782e636f6465636f67732e636f6d2f6769662e6c617465783f5c6c696d5f7b6e5c72696768746172726f772b5c696e6674797d2673706163653b5c73756d5f305e6e7b302e39355e6e7d2a3530303030302a622673706163653b3d2673706163653b32303030303030302673706163653b2d2673706163653b31353030303030)

We can calculate b = 1.85.

Assuming that the above solutions are implemented,
Let us assume that 1.85 ETP is generated each block as interest. Then, how should this 1.85 ETP be allocated? We have four options:
1.  Allocate it proportionately according to the value of deposit-generating transactions in the current block
2.  Allocate it proportionately according to the coin age of deposit-generating transactions in the current block
3.  Randomly select one depositor from the higher-value deposit-generating transactions in the current block. 
4.  Randomly select one depositor from the higher-coin-age deposit-generating transactions in the current block. 
Like PoS, options 3 and 4 can be categorized as game-theoretic systems. For increased system stability, we need to provide a proof under situations 3 or 4. 

Meanwhile, we are considering the possibility of designing a hybrid PoW/PoS system for Metaverse that would enable simultaneous PoW and PoS mining. With regards to this, we have analyzed [TwinsCoin](https://eprint.iacr.org/2017/232.pdf), [Hcash](https://h.cash/themes/zh-cn/dist/pdf/HcashWhitepaper-Rev0.8.1.pdf) and other mixed-mining tokens. 

### Mixed Mining Coin List
| Coin |  Conclusion | 
| --------------------------------- | ----------------- | 
| ETH |   To be studied             |  
|Hcash    |   Not many documents, code-based, requires further analysis       | 
| nevacoin |   Altcoin based on BTC, fairly old code             |  
| steepcoin.net  | Open-source with white paper. Can refer to their model            | 
|TwinsCoin    |  Open-source with white paper. Can refer to their model      | 
| emercoin|   Has white paper, can refer to their model              |  
| byzcoin  | To be studied            | 

TODO...

## Rationale
To be written.

## Backwards Compatibility
Existed deposit transactions is valid always, however, if this MIP done, system DO NOT accept old type deposit transaction any more.

## Test Cases
Test cases for an implementation are mandatory for MIPs that are affecting consensus changes. Other MIPs can choose to include links to test cases if applicable.

## Implementation
The implementations must be completed before any MIP is given status "Final", but it need not be completed before the MIP is accepted. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of "rough consensus and running code" is still useful when it comes to resolving many discussions of API details.

