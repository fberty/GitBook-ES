# HIP-10 [Signaling]: Create a decision locking mechanism.md
https://gov.proofofhumanity.id/t/hip-10-phase-2-signaling-create-a-decision-locking-mechanism/598
HIP: 10
title: Create a decision locking mechanism
author: @Mads
status: Signalling
created: 2021-05-16

Abstract
This proposal suggests creating a decision locking mechanism that will make decisions more difficult to reverse at a later date. This locking mechanism can either be applied to new or existing decisions.

Motivation
For some decisions, we need to signal to the world and ourselves that they are very unlikely to be overturned in the future and that it would require a lot of effort to do so. One such decision would be to, for instance, lock the $UBI issuance rate to ensure that people can forecast the value of the currency, improving stability.

Specification
There would be three ways of creating a locked decision.

In a new proposal, you would need to add the word “Locking” to the proposal topic, and add a separate section in the proposal, arguing why this decision should be locked.
For an existing approved proposal, the decision can be locked by creating a new proposal to lock the earlier decision.
An existing locked decision can be put up for a new locking vote to increase the reversal threshold further. This new vote requires a separate proposal.
In a locking vote, a minimum of 60 % approval is needed, if the approval is less then the proposal fails completely.

If the locking threshold is exceeded then a reversal threshold is set. The reversal threshold will be the approval rate of the proposal, rounded down to the nearest 5 %. So a proposal passing at 74.5 % would later require a 70 % vote to repeal.

If the reversal threshold would be set to above 90 % by the above rule then it is instead set to 90 %.

Rationale
This implementation allows the community to make reversing a decision very hard - but not impossible. The difficulty of reversing a decision scales with the amount of agreement at an earlier time. Consideration was also to include a requirement that some quorum of voters must participate in the vote, but this was dropped since this would make the difficulty of reversing a decision too linked to user participation which may vary in unpredictable ways over time. The locking of the issuance rate is postponed, since creating a locking mechanism AND using it on something so central would be too much for one vote.
