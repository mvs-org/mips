## Preamble

```
MIP: 16
Title: Metaverse Avatar Reputation System
Author: Patrick Tsoi, Penny Mao, Chang Liu
Type: Standard Track
Category: Core/ECO
Status: Draft
Created: 2018-10-29
```
**(The following is the Chinese version and will be translated into English later on）**
## Simple Summary
本文将基于对社会角色、社会地位与声誉的相关理论来阐述元界数字身份声誉系统的理论基础和模型设计。

## Theoretical Background
### Social Role、Social Status and Reputation (社会角色、社会地位与声望)
社会地位是指社会个人在社会上，根据其社会阶级所得到的荣誉和声望。社会地位可以通过自致或者先赋予两种方式决定。一种是通过自致地位，即透过自己后天的的努力争取回来的社会地位，或者指一个人在其一生中通过行使知识、能力、技巧等所取得的结果；二是先赋地位，即一个人是透过先天来自家族或者团体等承袭得到其于社会分层体系中所处的位置；先赋地位亦意指在某些社会中，一个人从出生起就被赋予无法改变的社会地位。在整个人类社会中有基于性别、年龄、种族、国别和家庭背景等的先赋社会地位。例如，某些家族基于巨大的物资财务而可能有着高知名度和声誉、某些成员以能干闻名于社会、以及坐拥巨大财富等特征，若一个人出生于其中，在成长过程里将会背负着很多期望。故此，他们会被赋予多种社会角色并加以训练，在这个逐步取得家族特征的过程中，他们将会被社会定位于这个家族之中。而职业所带来的地位则是可能个同时不属于先赋或自致地位的例子，它是一个人可以通过得到正确的知识和技巧而获社会定位到该工作的更高位置，从而建立个人在职业中的社会角色。

### Social Role in blockchain(区块链中的社会角色)
基于区块链的形成数据空间，个体或者团体（法人）可以建立属于这个数据空间的唯一的数字身份包括属于声望、信用和权利。通过区块链的技术使得每一个数字身份可以通过数字签名确权证明或背书。当个人或者团体唯一的数字身份拥有了签名私钥，可以在任何时候证明自己的身份，以后可以在许多区块链上的应用场景，如预订酒店房间、预订航班机票、使用共享服务、进行网络金融借贷等所有需要验明真身的地方，都可以用其唯一的数字身份证明。

另外，唯一的数字身份下可以记录使用者在区块链上多个应用的不同的（社会）身份/角色以及其历史行为，如某一个数字身份向另外的一个数字身份进行资金资产的转账；数字身份之间的借贷；数字身份之间的结婚登记；数字身份下技能、学历、职业发展登记验证等等。使得数字身份不仅仅是一个验证身份证明“我是我”的工具同时也是记录“我做过什么”的历史行为记录的载体。

### Reputation system in blockchain（区块链中的声誉系统）
针对社会角色、社会地位以及声望的关系描述和在区块链上的使用，声誉反映的的是个人或者团体的社会地位，社会地位的高低从而影响该主体在职业、教育、经济和权力的领域。而声誉系统是可作为基于区块链上的数字身份的一个是核心的价值应用，区块链可以通过链上的数字身份和声誉系统推动区块链上的应用场景和使用频率、用户可以通过自己的数字身份及行为历史来建立自己的声誉，区块链系统会基于数字身份在区块链上的行为如数字货币转账、数字身份的建立、区块链上的借贷、在数字身份上登记学历证明、结婚证明等等行为来增减数字身份的声誉值。数字身份背后的声誉代表其在区块链上的社会地位及声誉、而可量化的声誉系统更能够直接或间接与其他在区块链上的应用相互影响数字身份在这些应用中适用范围。

## Specification
### MVS Avatar Reputation System MARS （元界数字身份声誉系统)
区块链的到来，建立一个人人都可以信任的身份，甚至包括个人信用、个人权利，都可以第一次实现。通过区块链等数字签名来确权证明。当一个人只要拥有了签名私钥，可以在任何时候证明自己的身份，以后订酒店、订航班、参加考试、公司面试、网络借贷等所有需要验明真身的地方，都可以用一个区块链身份证搞定，且无法作假。元界的数字身份声誉系统（简称MARS）是基于元界区块链(MVS)和元界数字身份(MVS Avatar)建立的基于声誉纽带关系系统，MARS旨在增加可以元界数字身份使用的延展性，不仅仅用于数字身份之间的MST和MIT的转账，而且延伸数字身份在数字货币的借贷、数字身份在元界区块链上应用的功能区分等。

### Reference (市场参考）
目前市场上最主要的两大个人声誉信用评级机构FICO及芝麻信用。在银行业运用最广泛的就是FICO分数，这是由FICO公司拥有的一种计算模型，其具体细节并没有批露，综合以下几个要点来决定决定了您的信用分数。 

*1.还款历史 （35%）（payment history）*

*2.债务与收入比例（30%） (amount Owed）*

*3.信用史的长短（20%）（length of Credit History)* 

*4.新增的信用账户数量（10%）（New Credit Account)* 

*5.借款种类（10%）(types of credit used).*

FICO分的区间在300~850分之间，不同的得分档次意味着不同的违约概率。 体现在违约率上，FICO分低于600分，贷款违约比例为1：8；信用分数在700~800，违约比例为1：123；信用分大于800分的借款人，违约比例仅为1：1292。

而芝麻信用根据阿里旗下的消费类应用如淘宝、支付宝等数据建立一个信用分体系，主要的核心模块有五个包括：

*1.身份特征（15%）如公安实名认证，身份信息，信息稳定性等。*

*2.信用历史（35%）信用卡还款历史，微贷还款记录，水电煤缴费，罚单等。*

*3.履约能力（20%）如支付账户余额，余额宝余额，车产信息，房产信息等。*

*4.人脉关系（5%）如关系圈，朋友圈，信用水平，社交影响等。*

*5.行为偏好（25%）账户活跃度,消费层次,缴费层次,消费偏好等。*

芝麻分的分值范围为350至950，分值越高代表信用越好，相应违约率相对较低，较高的芝麻分可以帮助用户获得更高效、更优质的服务。


### Model Design（模型设计）
元界数字身份的声誉系统的设计将基于目前元界区块链功能/数据的维度如充值记录、转账历史、MST数字货币存量、MIT数字资产存量、发币历史等并参考目前市场流行的信贷风险评估模型建立。模型的框架基于多维度的权重模型，根据元界区块链上不同的应用（包括公链在内）的所有数据维度，都可以建立该应用（包括公链本身）
的声誉模型。本文以建立元界公链本身的信誉体系为基准。

### Dimension Selection 维度选择
根据以上对目前市场的声誉信用评级模型结合元界区块链和数字身份的功能，以下维度将被选择为元界MARS的评级维度。

*1.行为偏好（转账次数/周、充值次数/周、MIT发布资产/月、MST发币次数）占模型35%*

*2.履约能力（ETP账户地址资产量、MST资产量、MIT资产量）占模型30%*

*3.信用历史（矿工费支付数量/次）20%*

*4.人际关系（转账对象的数量）15%*

### Model Construction （模型构建）
本模型将以元界数字身份在元界区块链的行为数据及基础分为基础，通过评分卡模型的打分综合形成数字身份的声誉分数。模型公式如下：

MARS = Basic Marks + Personal Berhaviour *35% + Capability Performance *30% + Credit History *20% + Social Network * 15%




Pending

## Rationale
To be written.

## Backwards Compatibility
The main function of the The Metaverse Avatar Reputation System (MAR) is to reflect the MVS Avatar Data

## Test Cases
Test cases for an implementation are mandatory for MIPs that are affecting consensus changes. Other MIPs can choose to include links to test cases if applicable.

## Implementation
The implementations must be completed before any MIP is given status "Final", but it need not be completed before the MIP is accepted. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of "rough consensus and running code" is still useful when it comes to resolving many discussions of API details.

