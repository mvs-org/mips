## Preamble

```
MIP: 2
Title: Adjust reward rate of deposit function
Author: Chen Hao
Type: Standard Track
Category: ECO
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

## Specification
Fix a relative lower bonus rewards each block.


## Rationale
TODO...


## Backwards Compatibility
Existed deposit transactions is valid always, however, if this MIP done, system DO NOT accept old type deposit transaction any more.

## Test Cases
Test cases for an implementation are mandatory for MIPs that are affecting consensus changes. Other MIPs can choose to include links to test cases if applicable.

## Implementation
The implementations must be completed before any MIP is given status "Final", but it need not be completed before the MIP is accepted. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of "rough consensus and running code" is still useful when it comes to resolving many discussions of API details.

