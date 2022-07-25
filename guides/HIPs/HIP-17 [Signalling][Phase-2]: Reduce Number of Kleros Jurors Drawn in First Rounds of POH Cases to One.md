# HIP-17 [Signalling][Phase-2]: Reduce Number of Kleros Jurors Drawn in First Rounds of POH Cases to One
HIP: 17
title: Reduce Number of Kleros Jurors Drawn in First Rounds of POH Cases to One
author: William George
status: Phase-2
created: 2021-07-23

https://gov.proofofhumanity.id/t/phase-2-hip-17-reduce-number-of-kleros-jurors-drawn-in-first-rounds-of-poh-cases-to-one/933

Simple Summary
This proposal would adjust the parameter that controls how many Kleros jurors are drawn in the first round of disputes concerning Proof of Humanity registrations/removals.

Abstract
I propose to reduce the registration deposit by specifying that the initial round of a dispute in case of profile registration (or removal request) challenge only draws one juror instead of three.

This would be done by updating the following Proof of Humanity parameter.

Use changeArbitrator (specifically changing the _arbitratorExtraData) so that the initial round of a dispute only draws 1 juror.

Motivation
The goal here is to reduce the value required for deposits, to the degree that this is securely possible. Currently, in the first round of Kleros disputes for Proof of Humanity cases, three jurors are drawn to rule on the case. This number of jurors was initially selected to ensure greater stability in rulings and a lower number of appeals while the registry was in its infancy. The deposit that new submitters to the list have to make needs to include enough ETH so that if the submission is ultimately challenged and rejected, the arbitration fees paid to those jurors can be taken from that deposit. Hence, if one starts with initial panels of only a single juror to judge Proof of Humanity cases, this reduces the size of required deposits to submit to the list.

Recall that Kleros is a Schelling point based system and jurors are incentivized based on whether they are coherent with the final juror vote. Hence even when starting with only one juror, there is an incentive for that single juror to vote seriously because there is a potential for appeal. So if people think the juror voted incorrectly, there is likely to be an appeal and the first round juror would be rewarded or penalized based on what the appeal jurors decide. So far Kleros has used first round panels of only a single juror for Linguo (https://linguo.kleros.io/)

The negatives are that some borderline cases might not be appealed, so there is an added level of variability in terms of whether the first round juror represents how a larger panel would have voted, and that in (the minority of) cases where there is an appeal and you wind up back with a three juror panel anyway, there is an additional delay and some extra gas to have gone through the one juror round.
