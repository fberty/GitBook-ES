# [Binding] HIP-5: Adopt a proper PoH DAO Governance process to ensure HIP quality
[Link to HIP-5 proposal thread](https://gov.proofofhumanity.id/t/hip-5-adopt-a-proper-poh-dao-governance-process-to-ensure-hip-quality/393)

### Simple Summary

This proposal details a process for creating PoH DAO governance proposals and putting them up to vote.

### Abstract

This proposal provides a detailed structured process for PoH DAO governance proposals. Any individual or entity wishing to create a proposal and put it up to vote will need to go through those steps to ensure that its proposal is detailed enough to be voted on and its implementation enforceable.

### Motivation

The recent proposals on [PoH Snapshot page](https://snapshot.org/#/poh.eth) confused a lot of people in the PoH community. They lack any detailed description, link to a debate on PoH forum, proper structuring of the proposal and it is not clear if they are only for collecting signalling information or if they will be binding. Moreover, some of them invite people to vote on proposals that may not be technically feasible. This proposal will ensure only proposals and polls with the bare minimum quality will reach the snapshot page and avoid voter fatigue in the process.

### Specification

## PoH DAO Governance Process

The Proof of Humanity governance process is primarily conducted using the [DAO category](https://gov.proofofhumanity.id/c/democracy/7) on the Proof of Humanity Governance Forum. For a proposal to be accepted, it must successfully pass through three phases:

# Phase 1: Ideation

This phase facilitates an initial, informal discussion on PoH Forum regarding potential proposals to PoH DAO. You can initiate a proposal in Phase 1 by posting your idea in the[ DAO category](https://gov.proofofhumanity.id/c/democracy/7) with the phase-1 tag. This phase allows proposals to gather community insight for refinement before opening a formal poll.

**Duration:** Open-ended

**Passing Requirement:** For proposals to successfully pass from Phase 1 to Phase 2, there is no formal requirement. However, if a Phase 1 proposal discussion fails to garner any momentum from the community, it is unlikely to become a successful proposal.

# Phase 2: Specification

This phase requires proposals to be posted in a new dedicated thread the [DAO category](https://gov.proofofhumanity.id/c/democracy/7) using the Humanity Improvement Proposal (HIP) template. You can create a Humanity Improvement Proposal (HIP) easily by adding the HIP subcategory, after which your draft post will automatically be populated by a HIP template for you to fill in. You can move a proposal to Phase 2 by posting the HIP-# with the phase-2 tag.

The HIP template recommends that all proposals should contain the following fields when applicable , such as a Simple Summary, Abstract, Motivation and Specification.
In addition to these fields, Phase 2 proposals must also include a link to a 5-day long signalling poll on PoH Snapshot page about the proposal outcome (that contains the proposal text as well as a link to the HIP post on the PoH Forum), and it must include the option Make no changes. The Phase 2 proposal poll on Snapshot **should be prefixed by [Signalling]** to differentiate them from binding Phase 3 proposal votes*. In order to be eligible to signal in the poll, community members must be registered in the PoH registry.

>   *In the near future, if we are able to create polls on the forum only open to Discourse accounts linked to a PoH profile, then the signalling poll could be done on the forum.

**Duration:** 3 days

**Passing Requirement:** For proposals to successfully pass from Phase 2 to Phase 3, there must be one outcome with a relative majority of votes on the forum poll. If the relative majority of votes on the forum poll indicates the result Make no changes, the proposal will not pass to Phase 3.

# Phase 3: Consensus

This phase opens proposals to two signalling methods for token holders. You can move a proposal to Phase 3 by editing the HIP post from the previous phase to reflect the snapshot signalling poll result that received a relative majority of votes and by updating the proposal’s tag to phase-3. This serves to refine the proposal for the final phase.

Additionally, a PoH DAO proposal on Snapshot page must be created (that contains the proposal text as well as a link to the HIP post on the PoH Forum), **it should be prefixed by [Binding]** and it must include the option Make no changes. In order to be eligible to vote for the proposal, community members must be registered in the PoH registry.

**Duration:** 7 days

**Passing Requirement:** For proposals to be accepted in this final phase, there must be one outcome with a relative majority of votes in the Snapshot proposal. If the relative majority of votes on the proposal indicates the result Make no changes, the proposal will not be accepted and considered closed.

Any snapshot proposal not following these guidelines can be considered non-binding.

Many thanks to teams in the ecosystem including Gnosis, Balancer and Uniswap, which inspired this governance process.

# HIP Template

    HIP: <Number to be assigned>
    title: <HIP title>
    author: <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s),
    status: Draft
    created: <date created on, in ISO 8601 (yyyy-mm-dd) format>
    requires (*optional): <HIP number(s)>
    replaces (*optional): <HIP number(s)>

### Simple Summary

(Required for Phase 1)

If you can’t explain it simply, you don’t understand it well enough. Provide a simplified and layman-accessible explanation of the HIP.

### Abstract

(Required for Phase 1)

A short (~200 word) description of the issue being addressed.

### Motivation

(Required for Phase 1)

The motivation is critical for HIPs that want to allocate funding or change the PoH DAO. HIP posts without sufficient motivation may be rejected outright.

### Specification

(Required for Phase 2)

The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow for it to be reasoned about by participants in the PoH DAO.

### Rationale

(Recommended for Phase 2)

The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.

### Implementation

(If necessary, recommended for Phase 3)
