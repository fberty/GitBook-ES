# HIP-13 [Signaling, Phase-2]: Adopt a management onboarding procedure.md
HIP: 13
title: Adopt a management onboarding procedure
author: @Mads
status: Phase-2
created: 2021-05-21
amends: HIP-2

https://gov.proofofhumanity.id/t/hip-13-phase-2-adopt-a-management-onboarding-procedure/658

Simple Summary
This proposal makes rules for how to hire the management of the DAO, excepting this as a special case of the general hiring procedures.

Abstract
The management onboarding procedure suggested here is designed to allow applicants to request the resources they need and describe their plan to finance these resources. They can describe who they need to be hired - filling open positions as well as creating new ones. They can suggest dedicated budgets for specific purposes. They also need to describe how these resources are paid for. The budget and financing plan can be as slim (hire me for PM, we will figure it out later) or as expansive as the proposer desires.

The procedure also sets a way to decide when we pass on to a decision. We use polls to decide how much time we need to decide/wait for more applications, when the date comes we create a poll to either pass to a decision or extend the application process.

Motivation
This proposal is inspired by the applications that the DAO received to the product manager position. Two of the applicant, @paulaberman and @HBesso31, applied to the position with one (@paulaberman- Sofia Cossar) or several (@HBesso31 - Ryan Cwynar/Cami Arias/Anna Kaic) required team members.

This introduces a bit of a chicken-and-egg problem since the DAO is currently only authorized to hire employees individually (through the HIP-2 1) procedure but the applicants will only agree to be hired if they can have their team along. This proposal allows for the flexibility to accept such applications.

In addition, this proposal also creates a clear path towards a decision by regularly forcing a vote on whether we should move to a decision. This way we may keep the process open, but still signal to the applicants how close we are to being ready, giving a signal of how likely they are to get a decision.

Specification
Amending HIP-2: This process is an exception to HIP-2 because it allows hiring by the onboarding plan. This exception should be added to HIP-2.

Application:

A new thread is created for management onboarding or an existing one is designated for the purpose.
A decision/re-evaluation decision is made through a snapshot poll.
The re-evaluation poll will be “Are we ready to decide on a PM?”, answers “Yes” or “No - extend 1/2/4/8/16 weeks”.
If the answer is No we will use the median value of the poll for the number of weeks for the next re-evaluation date (“Yes” counts as 0).
If the answer is “Yes” we will close for further applications.
If an application comes in during voting, a full week (from the time of the application) must be available for discussion of the new candidate before moving to the next phase.
An application must describe their Onboarding plan:

How to fill open positions (specific people or the process)
Alternatively, that which open positions should be closed.
A budget for operation for at least one year.
A financing plan for at least one year.
Proposer Selection

A 7-day vote is created with all applicants (their handle in Discourse) in random order. “Which is your preferred PM?” Answers (“Applicant 1”/“Applicant 2”/“Applicant 3”)
The applicant with the highest vote count will become the current “Proposer”.
Onboarding:

The proposer will create a thread with the final onboarding plan which is allowed to be changed from the original application.
The Proposer must within one week create a snapshot poll with the title “[Binding] Onboard [Applicant Name]”.
The entire Onboarding plan must be pasted in the snapshot poll.
On rejection, the applicant with the next highest vote count becomes the new proposer and the application Onboarding phase is repeated.
If all candidates are rejected we reopen for the application phase.
Rationale
This process is a compromise between setting a deadline, which will allow candidates to plan their lives and keeping our options open. The candidates know when a re-evaluation occurs, and if we do not close for applications, at least they will get an indication of how close we were to closing and a new date giving them more feedback to plan.

The poll created by @paulaberman on whether to allow teams came back positive so this process allows for such a proposal. If you don’t like a team proposal, you are free to vote against it and/or vote to extend the application period if only team applications are in.

I considered making the proposal repeal HIP-3, however, this is not needed. HIP-3 simply defines two open positions. If these open positions (not specifying full-/part-time) are incompatible with an applicant’s plan then the applicant must argue why these positions should be closed as part of the Onboarding plan.

Implementation
Any member can take the actions to advance the process as long as the requirements are fulfilled.
