## Preamble

```
MIP: X
Title: Digital Aseets Lock-Unlock Model
Author: Frank Su
Type: Standard Track
Category: ECO
Status: Draft
Created: 2018-04-11
```

## Simple Summary
In fact, the Digital Aseets Lock-Unlock model is the function combinated by MIP-3(Digital Assets Secondary Issue), MIP-7 Digital Aseets - Lock), and MIP-8(Digital Aseets - Unlock). We decide to list a series of adjustable parameters for user to adjust by themselves, like Issue/issuance quantit, Freeze quantity, Release period, etc.
## Motivation
Customized asset locks and batch unlocks requirements, allowing users more flexibility to set their own assets.

## Abstract
At the present stage, the following 3 models are set up for users to choose.
1. Quantitative Release Model
1. Fixed Inflation rate Release Model
1. No Lock Model

These models can be choosen in below function：
1. Issue
2. Secondaryissue
3. Swap

## Specification
First of all, in order to facilitate the description of subsequent calculation formulas, we define the following parameters in a unified way：
IQ：Total issue/secondaryissue quantity at this time, must >0
LQ：Total lock quantity at this time, must >=0
LP：Total lock period, in Day units, must >0 and be the integer number
UC：Unlock period, in Day units, defines the unlock interval. For example, UC = 30 meant that parts of assest will be unlocked every 30 days, must >0 and be the integer number
UP_t: Unlock Percentage in period t
UQ_t: Quantity of Unlocks in period t
IR_t: Inflation Rate in period t

Following limiting logic will be added below：
1. IQ and LQ are required parameters and must be filled in by users while asseets issuing or secondaryissuing
2. When LQ > 0, LP/UC is required. UP_t, UQ_t, IR_t are dynamically calculated and recorded according to the selected model background.

### Quantitative Release Model

#### Summary：
This model unlock Token with a fixed quantity release model for each period. At the same time, the market's inflation rate will also theoretically change from 100% to 0%.

#### Model Logic：
After choosing this model, the IQ/ LQ/ LP/ UC must be filled and greater than 0. The background automatically calculates and saves the UP_t (UQ_t) data according to the following formula. In this mode, UP_1=UP_2=... =UP_t (UQ_t). Thus, Thus,only UP_1 (UQ_1) stored in the background is enough:
![p3](https://images-cdn.shimo.im/UTC37744UJoVHLCn/image.png)

For example, user issued and locked all 20 million A-Token on 1st Dec 2017. The total lock period is 360 days and will be released each 30 days. Then, the program can get the data as below:
![p3](https://images-cdn.shimo.im/UgM92otoER0pgWlo/image.png)

The subsequent unlocking program will unlock the A-Token according to the same UQ=1666666.67 every 30 days, and the last issue will unlock all remained lock A-TOKEN as the LQ cannot be divied by the whole release period(LP/UC = 12).

### Fixed Inflation rate Release Model

#### Summary：
This model unlock Token with a Inflation rate release model for each period and dynamically adjust the Quantity of unlocks per period.

#### Model Logic：
After choosing this model, the IQ/ LQ/ LP/ UC/ IR_t must be filled and greater than 0. The background automatically calculates and saves the UP_t (UQ_t) data according to the following formula. In this mode, IR_1= IR_2=…= IR_t. Thus,only IR_1 stored in the background is enough:
![p1](https://images-cdn.shimo.im/1mIR9hf3CgwAJfM9/image.png)

For example, user issued and locked all 20 million A-Token on 1st Dec 2017. The total lock period is 360 days and will be released each 30 days. Also, he hopes that each unlock will only bring 8% IR for his token. Then, the program can get the data as below:
![p2](https://images-cdn.shimo.im/5tueFZsDKkkgI56z/image.png)

The subsequent unlocking program will unlock the A-Token according to the each UQ_t every 30 days, and the last issue will unlock all remained lock A-TOKEN as the LQ cannot be divied by the whole release period(LP/UC = 12).

### No Lock Model

#### Summary：
This model provides a normal Token mode without any locking.

#### Model Logic：
After choosing this model, IQ must be filled and greater than 0, while LQ is 0. In fact, there is no requirement for asset lock and unlock.

For example, user issued all 20 million A-Token on 1st Dec 2017 without any locking. It means that all these 20 million Token can be directlly circulated on the chain. Then, the program can get the data as below:
图片: https://images-cdn.shimo.im/uU97rtk6NQYUr1dR/image.png

## Rationale
To be written.

## Backwards Compatibility
New functions, no compatibility requirements.

## Test Cases
To be written.

## Implementation
To be written.

## Copyright
To be written.


