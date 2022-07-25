# HIP-18 [Signalling]: Communication roles.md
```
HIP: 18
title: Communication roles
author: @clesaege
status: Phase 2
created: 2021-06-17
conflicts with: HIP-16
languages: EN
```

# English version

## Simple Summary

This HIP institutes a mechanism to determine the position of administrator in the social communication tools that are recognized as official by the DAO, either social media (twitter, reddit) or communication channels (telegram groups).

## Abstract

In order to further decentralize positions of enforcement within the DAO, there is the need to create mechanisms in which the role for administrator of the communication channels **generally regarded as official** (*GRAO*, from now on, defined in the Specification section).

## Motivation

Following the spirit of HIP-5, which creates a framework for management of the DAO without altering the smart contract, I propose a better mechanism for establishing enforcing roles within the all recognized channels of communication.

## Specification

### Definitions

1. Administrative role or admin: the position that a person has over a channel of communication, it being social media accounts, forums, instant messaging groups. In this position, the person has privileges to enforce policies or the convened rules of these channels and include muting, removal or admitting the participation of the members of the group, along with other administrative tasks.
2. Channel Generally Regarded as Official (GRAO): a volunteer status for any of the channels in the scope of this HIP in which there is an agreement of the channel owner/creator to be acting on behalf of Proof Of Humanity.

### Scope

Roles for admin positions for each of the GRAO channels of communication would be temporary roles and elected from the community. These are for example (non exhaustive list):

* Discord forum
* Twitter
* Facebook groups
* Reddit
* Discord
* WhatsApp
* Instagram
* Telegram groups, users and channels

### Elections

1. Elections are made separately by platform.
2. Before any election is held on a platform, the mission board assumes the administrative powers (each board member counting as an administrator).
3. For platforms controlled by the mission board, 3 members wishing to be candidate can call for an election.
4. When they do so, there is a 1 week period to let time for other candidates to apply.
5. Elections are made using quadratic voting (negative votes are allowed). *
6. Each Human will receive 99 voting credits.
7. The top 3 candidates with a positive score would be elected.
8. If there are less than 3 candidates with a positive score, there may be less than 3 admins for this channel.
9. Admin roles are to be elected for a period of 1 year.
10. In case the mission board believes some administrator is harming the Proof Of Humanity interest, it can call an emergency 24h vote to remove an administrator.

* Currently we will use tokenlog for those votes. If a dedicated voting system becomes available, the DAO could switch to use it. Note that in the current state of tokenlog the interface may not natively support delegations (either not count delegations or allows both the elector and delegate votes to be counted resulting in a double count), we may initially need to run a script to give the results (accounting for delegations) but if possible a proper interface would be used.

## Administrators obligations

Administrators acknowledge that access to communication channels or profiled labelled as “admin” give them an additional power which comes with additional responsibilities. They are expected to behave as ambassadors of the project. In addition to following the appropriate codes of conduct:

* They should refrain from expressing virulent opinions about Proof Of Humanity or related projects with their admin accounts.
* They are subject to higher standards in term of good conduct (ex: avoiding excessive profanity).

This doesn’t preclude them from formalizing criticism on Proof Of Humanity. However, it should be done either in a purely technical manner, or using a non-admin account.

## Conflict with [HIP-16](https://gov.proofofhumanity.id/t/phase-3-hip-16-make-admin-roles-of-communication-platforms-eligible/786)

This proposal is an alternate version of HIP-16 with a few modifications. In case both those proposals were to be accepted, another direct vote (which would not have to go through the classic HIP process) would be required:

> Which HIP should take precedence?
>
>
>
> * HIP-16
> * HIP-18

## Delegations

Administrators can delegate their administrative powers to anyone they see fit. They can remove delegations they made at any time without having to provide any justification.
In case an elected administrators disagree on a delegation made by another administrator, the administrators conduct a vote. In case of removal or tied result, the delegate have their delegation removed.

## Rationale

Currently, the admin positions in communication channels *GRAO*, were subject to the initiative of the person that first created the channel, (telegram, reddit). These roles right now are virtually permanent, without rules that govern their time in that position, or how or why their roles were assigned. This creates space for centralization and the possibility of indefinite perpetuation in the position, among other issues that arise from this permanence in their role (silencing opposition, pushing a specific agenda, creating a hostile environment, etc.). We’ve seen that different admins sometimes have significant divergence of opinion about how channels should be handled and it had led to a few virulent discussions. This proposal establishes a clear and objective way people are added or removed from admin positions.
This proposal is mainly taken from HIP-16 but with some changes in the details to make it more practical (allowing delegations, having higher standards for administrator conduct) and to clarify the voting method.
