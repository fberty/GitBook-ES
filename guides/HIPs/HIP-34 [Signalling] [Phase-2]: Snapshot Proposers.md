# HIP-34 [Signalling] [Phase-2]: Snapshot Proposers
https://gov.proofofhumanity.id/t/phase-2-hip-34-snapshot-proposers/1426
```
HIP: 34
title: Snapshot Proposers
author: Clément Lesaege
status: Phase-2
created: 2021-12-16

```

### Simple Summary

This proposal ensures that the board doesn't have discretionary power to censor proposals by: 
- Extending the list of proposers.
- Specifying that proposers are simply administrative agents and do not have discretionary powers.
- Providing a fail-safe in case all proposers were to maliciously censor proposals.

### Motivation

Snapshot used to allow anyone to make proposals while allowing board members to remove proposals. However, as PoH got more traction and its governance watched by more people, it became attractive for spammers to use the space for spam.

The [first attempt to prevent submission spam was rejected](https://snapshot.org/#/poh.eth/proposal/QmRoiqcyDeJkUxG4Go5Sr8gHUziCqLc66HdVPuuT6ZcEAE) but this still left a legal void on how snapshot should be administrated.

As spamming became more intense, a board member changed snapshot settings to prevent people other than board members to submit proposals.

This now lead to the risk of the board having the power to censor proposals.


### Specification

* The main snapshot page is reserved for official proposals (following HIP-5 and its possible amendments).
* All proposers are given the technical ability to put proposals to vote.
* Proposers are comprised of:
  * Board members and their delegates.
  * People employed by the DAO.
  * People elected as proposer through a proposal.
* It is possible for proposers to be anonymous.
* After being informed of a proposal request, a proposer must verify that it complies with HIP-5 (and its potential amendments), if it does, he puts it to vote without delay. Proposers do not have any discretion in whether a proposal is put to vote or not. It is a purely administrative task to avoid spam / invalid proposals from cluttering the interface.
* In case a valid proposal were not to be put to vote within a week by any proposer, anyone can create a new snapshot page with a 10 days proposal changing the official snapshot page and electing one or multiple new proposers. It should include “Make no change” and “Change the snapshot page and add proposers”. It should also be displayed on the forum.
A proposer can also post this proposal on the current snapshot page.
If the amount of  “Change the snapshot page and add proposers” votes on any of the snapshot page exceeds the amount of “Make no change” on both snapshot pages, the proposal is accepted.
In case no proposal is created by a proposer within the voting period of the proposal on the new snapshot page and the amount of “Change the board composition and snapshot page” exceeds the amount of “Make no change”, the proposal is also accepted.
* In case of proposals/votes being censored by another mean (ex: snapshot issue, issue with the snapshot administrator not adding proposers correctly) a similar process can be used to change the voting platform to a new platform.
