# HIP-16 [Binding]: Make admin roles of communication platforms eligible.md
# English version
## Simple Summary

This HIP institutes a mechanism to determine the position of admin in the social communication tools that voluntarily want to be recognized as official by the DAO, either social media (twitter, reddit) or communication channels (telegram groups).

## Abstract

In order to further decentralize positions of enforcement within the DAO, there is the need to create mechanisms in which channels of communication get the seal of “Community Managed [channel]” (i.e. “PoH Subreddit, Community Managed”).

## Motivation

Following the spirit of HIP-5, which creates a framework for management of the DAO without altering the smart contract, I propose a better mechanism for establishing enforcing roles on all recognized channels of communication.

## Specification

### 1. Definitions

1. Administrative role, administrator, or admin: the position that a person has over a channel of communication, it being social media accounts, forums, instant messaging groups. In this position, the person has privileges to enforce policies of the convened rules of these channels and include muting, removal or admitting the participation of the members of the group, along with other administrative tasks. Although they are free to do so, it is not the responsibility of the person holding the admin role to moderate dialogue or content creation, which is a role more commonly known as community manager, moderator, facilitator, etc. An admin may be assigned the role of moderator by the authority responsible for that (Product Manager, Mission Board), but moderators assignment and mechanisms are outside of this HIP.
2. Community-managed channel: a volunteer status for any of the channels in the Scope of this HIP in which there is an agreement of the channel owner/creator to be associated with PoH. It is accompanied by a badge or a seal or any piece of text that clearly recognizes them as such.

### 2. Scope

Roles for admin positions for each of the Community-Managed channels of communication would be temporary roles and elected from the community. These include (non-exhaustive list):

* Discourse forum
* Twitter
* Facebook groups
* Reddit
* Discord
* WhatsApp
* Instagram
* Telegram groups, users and channels

### Elections

1. Elections are made separately by platform.
2. Elections should be done in the Tokenlog platform ([here's the current implementation](https://tokenlog.xyz/Proof-Of-Humanity/proof-of-humanity-web), new repositories will be created on Github solely for the purpose of the Administrator election on each of the platforms).
3. Elections are ongoing.
4. Elections are made using quadratic voting (negative votes are allowed).
5. Each Human will receive 99 voting credits.
6. Ideally, there should be 1 elected admin for every 500 users in a channel (since the position is voluntary, there might be less than 1 elected admin per 500 users).
7. The top candidates with a positive score will take their positions (e.g. on a channel with 2.715 members, the top 5 candidates with a positive score will become the official Administrators).
8. Each time one of the official Administrators lose their position on Tokenlog's ranking, the next candidate to come up in the rank will gain the official role as Administrator.
9. Admin roles should be registered individuals in Proof of Humanity.
10. Roles are only revocable for security reasons or serious offenses to the community. The Mission Board can call an emergency voting of 24h in Snapshot. Admins revoked in this way cannot re-apply for the role in the next term.
11. Admin roles are not moderator roles, therefore do not require to suppress their opinions in debates, as long as they follow the code of conduct established for that channel. Mere opposition to that admin’s opinion should not be grounds for the admin to ban that person.

### Administrators obligations

Administrators acknowledge that access to communication channels or profiles labelled as “admin” gives them an additional power, which comes with additional responsibilities. They are expected to behave as ambassadors of the project. In addition to following the appropriate codes of conduct:

* They should refrain from expressing virulent opinions about Proof Of Humanity or related projects with their admin accounts.
* They are subject to higher standards in terms of good conduct (ex: avoiding excessive profanity, or engaging in debates on topics outside of Proof of Humanity, such as politics or religion).

This doesn’t preclude them from formalizing criticism on Proof Of Humanity. However, it should be done either in (i) a technical and dispassionate manner, and preferably offering constructive solutions, or (ii) using a non-admin account.

### “Community-managed” status implementation

1. The owner of any channel of communication within the scope of this HIP can contact the Mission board and apply for the “Community-managed” status.
2. A call for volunteers is offered in the channel and those members participate in the election process.
3. Once that process is finished and the elected members are occupying their roles, that channel receives the “community managed” badge, and a link to that channel will be provided in Proof of Humanity project site, and referenced throughout the rest of the channel's ecosystem.
4. Failure to comply with any aspect of this HIP would trigger the removal of that channel from the “community managed list”

### Special first condition

For their significance, and to spearhead the value of having the “Community managed” status, the following channels should enter the admin selection process effective immediately:

* Telegram Group Proof of Humanity https://t.me/proofhumanity
* Telegram Group Proof of Humanity en Español https://t.me/proofofhumanityenespanol
* Telegram Group Proof of Humanity Chinese https://t.me/ProofOfHumanityCN
* Telegram Group Proof of Humanity Portuguese https://t.me/poh_pt
* Subreddit Proof of Humanity https://www.reddit.com/r/proofofhumanity

## Rationale

Currently, the admin positions in communication channels that have grown to the thousands of users, were subject to the initiative of the person that first created the channel, (telegram, reddit). These roles right now are virtually permanent, without rules that govern their time in that position, or how or why their roles were assigned. This creates space for centralization and the possibility of indefinite perpetuation in the position, among other issues that arise from this permanence in their role (silencing opposition, pushing a specific agenda, creating a hostile environment, etc.). Some object that this is not an important role to be considered for election, or that this will lead to voting fatigue. There are enough reasons to believe that this proposal will not lead to this sort of problems.

----
## Version en Español
Disponible en este link: https://gov.proofofhumanity.id/t/phase-3-hip-16-make-admin-roles-of-communication-platforms-eligible/786
