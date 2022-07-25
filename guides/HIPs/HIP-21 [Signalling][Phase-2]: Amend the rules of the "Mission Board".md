# HIP-21 [Signalling][Phase-2]: Amend the rules of the "Mission Board"
HIP: 21
title: Amend the rules of the “Mission Board”
author: @Mads
status: Phase-2
created: 2021-07-06
amends: HIP-7

https://gov.proofofhumanity.id/t/phase-2-hip-21-an-amended-mission-board/853

**Summary**
This proposal is to amend the Mission Board, instituted by HIP-7, by clarifying the scope of power and adding rules for dispute resolution. A 5th member and a tie-breaking vote are also added for the case when the board cannot come to unanimous consent. 

**Abstract**
The Mission Board needs to function also in the case when decisions are disputed. Therefore we need some simple rules for what happens when there is no consensus. This proposal clarifies what happens in case of dispute, clarifies the limit to the power of the board, and adds two tie-breaking mechanisms - a 5th board member and a tie-breaking vote.

**Motivation**
A board member contacted me about concerns about the functioning of the board. HIP-7 made the board sound too much like management, and the powers could be interpreted too broadly. In addition, it assumed that the board would function completely without disputes, which was a bit naive. So this proposal seeks to address these issues by adding mechanisms for dispute resolution. The biggest mechanism is adding a 5th board member for election immediately, making the board an uneven number.  

**Specification**
Amend HIP-7 with the following paragraphs:

Power Scope:
* The board is NOT management cannot direct any actions unless it relates to a decision by the DAO (Such as if a proposal is correctly passed according to HIP-5).
* The board has, however, broad power to interpret the rules of the DAO, including filling in details not specified in a proposal. (Such as a proposal calling for an election and deciding to hold a quadratic voting election with pre-announced candidates).

Dispute resolution:
* A board member can judge whether a proposal or action follows the rules of the DAO. When acting in this way, the board member must clearly state it (instead of just stating an opinion as a normal PoH member).
* Any member can ask another board member to weigh in on a judgment.
* If the board members disagree on the judgment, they will need a majority vote among the board members to make a final decision.
* A tie-breaking vote will be held by the board member whose seat will be up for election at the latest date. (Tie-breaker is added for the case when a seat is unoccupied or a member abstains from voting)

Election rules:
* A board member can step down, leaving their seat unoccupied.
* Unoccupied seats are immediately up for election.
* A seat can maximally be occupied for 5 years before a new election for that board seat is required. (The interim board members are still limited to 1 year as pr. HIP-7)

A 5th member:
* An unoccupied 5th seat is opened on the board.

**Rationale**
This proposal attempts to contradict nothing in HIP-7, neither the spirit nor the letter. This was chosen over a complete revision to keep the governance more consistent.
