# HIP-30 [Binding][Phase-3]: Update PoH Governor Deposit Cost
```
HIP: 30
title: Update PoH Governor Deposit Cost
author: @WGeorge @santisiri
status: Phase 1
created: 2021-09-28
conflicts with: None
languages: EN
```

## Simple Summary

The [Kleros Governor contract](https://governor.kleros.io/Proof%20of%20Humanity) managing the funds of the Proof of Humanity DAO currently has a deposit requirement of 13.0005 ETH. We propose to reduce this deposit requirement in alignment to a [Kleros KIP 43 proposal](https://forum.kleros.io/t/kip-43-parameter-updates-august-2021/629) to 4.1 ETH

## Abstract

The target for this parameter is supposed to be more on the order of 10k usd originally, so it should be brought down somewhat to account for increases in ETH prices since the last time the parameter was updated. The task of reviewing governor updates is technical, and extremely sensitive, so the bounty for challengers needs to be quite high. Nonethless, it doesn't need to be as high as 13 ETH today. 

Kleros has proposed on KIP-43 to reduce the governor deposit fees to 4.1 ETH and we recommend following the same path for Proof of Humanity. 

## Implementation

Update Proof of Humanity's Kleros Governor `submissionBaseDeposit` to 4.1 ETH.
