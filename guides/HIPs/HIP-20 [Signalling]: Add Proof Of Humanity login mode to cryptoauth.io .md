# HIP-20 [Signalling]: Add Proof Of Humanity login mode to cryptoauth.io
```
HIP: 20
title: Add Proof Of Humanity login mode to Cryptoauth 
author: Greg (@xunkulapchvatal)
status: Phase 2
created: 2021-06-09
```

# Simple Summary

Implement dedicated UI and simple configuration option for “Login with Proof Of Humanity” in Cryptoauth.

# Abstract

Currently when you want to allow people to login to your Discourse, WordPress, etc, using their Ethereum wallet and limit it to only people with PoH, you can use built-in Cryptoauth token restrictions mechanism. This works, but it’s far from ideal.

The user is exposed to more details (like proxy contract address) than necessary and looses the feeling of integrity. He clicks “Login with Proof Of Humanity” button, but nothing on login screens indicates that he is still in this (PoH login) process.

On the integration side, an integrator is required to ask me (Greg) to set token restrictions for given integrations instead of being able to set them on their own during configuration process.

Dedicated mode will improve end-user experience and allow for much easier integration of Proof Of Humanity login to new web applications.

# Motivation

I want to provide simple way for people to be able to add “Login with Proof Of Humanity” to their websites. I believe this will be beneficial both for Cryptoauth project (it will be much easier to use it) and to Proof Of Humanity project (it will be much easier for communities to adopt it in their forums and other websites).

# Specification

The work in this proposal can be split into two categories: Configuration backend and Dedicated UI. Self-registration portal that would further enhance the integration experience is out of scope for this proposal.

## Configuration backend

In order to make the integration as simple as possible I decided that providing “scope” based configuration option would be the best approach.

During the configuration of Discourse or other software to use Cryptoauth, you would pass proof-of-humanity in scope parameter and this would force Cryptoauth to switch from default mode to “Login with Proof Of Humanity” mode.

The work here is mostly on the backend services that need to interpret this configuration and pass it to UI.

## Dedicated UI

UI changes are mostly described in designs.
Additionally, the wallet select screen would also need to change and address select screen would need to indicate which addresses are verified with PoH.
Wallets can provide multiple addresses for login and user should see clear information which of the addresses from his wallet are valid for PoH login.

# Rationale

Adding PoH login option to Cryptoauth looks like the easiest and the fastest way to enable simple “Login with Proof Of Humanity” for all interested communities.

## Login with Proof Of Humanity as separate product

There is an option to create separate product that would deliver the same functionality (separate domain) and to deploy it independently from Cryptoauth (either maintained by me or by external team)

This was rejected as requiring more work for initial release.
This option would still be available even after PoH login will be added to Cryptoauth main codebase as both solutions share much of the required work.

# Maintenance & Support

I’m able to provide support for users (via Crisp integration in Cryptoauth) and maintain the system as part of normal Cryptoauth operations, but I will require dedicated contact person to pass them issues related to PoH itself.

# Cost

## Development

Cost: 8k USD (~1 month/one developer).
This includes development, testing, operations costs during development and producing materials like configuration guides etc.

## Technical support

Cost: 3k USD ($500/mo for 6 months)
The initial period of 6 months after the deployment is when I would provide technical support for users and provide fixes for any found bugs. After this period the support for “Login with Proof Of Humanity” would be included in normal Cryptoauth operations.

## Total Cost

The total cost amounts to 11k USD

## Links

- [Proposal thread at gov.proofofhumanity.id](https://gov.proofofhumanity.id/t/phase-1-hip-add-proof-of-humanity-login-mode-to-cryptoauth-io/784)
- [Designs](https://www.figma.com/file/LCKgQFI97FdWFUvFR9XX8s/POH)
