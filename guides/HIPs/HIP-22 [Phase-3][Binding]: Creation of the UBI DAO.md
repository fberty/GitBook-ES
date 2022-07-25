# HIP-22 [Phase-3][Binding]: Creation of the UBI DAO
```
HIP: 22
title: Creation of the UBI DAO
author: @santisiri @RustyTheGamer @clesaege @fraserdscott
status: Phase 3
created: 2021-07-01
conflicts with: None
languages: EN
```

## Simple Summary

This HIP will split the governance of the UBI smart contract from the governance of the Proof of Humanity protocol by creating a new DAO specifically for the monetary policy and technical innovations required for the Universal Basic Income ERC20 smart contract (UBI). 

## Abstract

As Proof of Humanity evolves, the protocol itself will maintain its `1 person 1 vote` governance model using liquid democracy but it will only have influence over the Proof of Humanity protocol itself and no longer influence changes over the UBI token. The UBI token will have moving forward a specific DAO of its own, where holders of UBI will be able to vote with their stake and thus make decisions that will have influence over the [UBI smart contract](https://etherscan.io/token/0xdd1ad9a21ce722c151a836373babe42c868ce9a4).

## Motivation

In order to increase the demand-side pressure, improving the utility of the UBI token by making it useful for governance decisions that influence its own smart contract shall have a positive impact in price over the long term and incentivize long term accumulation from investors and holders. Governance staking has proven to be an effective influence for long term holding across multiple DeFi projects and from a legitimacy perspective, it makes sense that those with "skin in the game" get to advance the interests of UBI token holders.

Also, taking into consideration that UBI gets airdropped evenly to every verified human on Proof of Humanity, we don't consider this puts at risk the democratic ideals that we pursue as a community. On the contrary: this is aimed at increasing the value of UBI over the long term which shall ultimately benefit every Proof of Humanity member.

## Specification

###  The DAO

1. UBI shall have a Snapshot page of its own where holders of UBI that are verified Proof of Humanity accounts will be able to vote with their holdings of UBI.  

2. A Kleros Governor shall be setup to enforce on-chain the off-chain votes expressed on the UBI DAO.

3. The DAO shall implement a Quadratic Voting scheme where holders will be able to vote with their stake but whales will be mitigated from excessively influencing the outcome of votes since the votes will be computed using the following formula: 
```
(voting power = sqrt(balance) * isHuman())
```

4. From the treasury of the Proof of Humanity DAO that originally consisted of 4 million UBI, 50% will be sent to the UBI DAO (2 million UBI). This will not have impact over the ETH or any other assets currently under the custody of the Proof of Humanity DAO.

### Implementation

* The [UBIProxy.sol](https://github.com/DemocracyEarth/ubi/blob/master/contracts/UBIProxy.sol) smart contract will be used to create the UBIVOTE token as a proxy for the Snapshot page of UBI since it follows the voting formula specified above.

* A Snapshot Page for UBI DAO will be created using the UBIVOTE token.

* A Kleros Governor will be created to enforce on chain decisions made on the UBI DAO — The UBI Governor.

* The UBI token smart contract proxy will be managed by the new UBI Governor created for the UBI DAO.

* 2 million UBI from the [Proof of Humanity DAO treasury](https://etherscan.io/address/0x327a29fce0a6490e4236240be176daa282eccfdf) will be transfered to the UBI Governor.  

### Additional Notes

Large holders of UBI that are not verified as Proof of Humanity members won't be able to participate in the DAO. This means that in order to engage with the DAO, UBI holdings must be used directly from a verified Proof of Humanity address. This will help understand the distribution of UBI across multiple accounts and measure the Gini coefficient of the community over the long term. 

### We Are United 💪

Last but not least, this is by no means a split of the Proof of Humanity & UBI projects. They both share the same community and must remain connected through the User Interfaces that connect their smart contracts together so current and future users will begin accruing UBI once they finalize their profile.
