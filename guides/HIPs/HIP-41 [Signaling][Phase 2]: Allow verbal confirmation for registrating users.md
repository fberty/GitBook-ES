# HIP-41 [Signaling][Phase 2]: Allow verbal confirmation for registrating users
>HIP 41
>Title: Allow verbal confirmation for registrating users
>authors: avsa.eth and nicobilinkis.eth
>Status: Phase 2
>Created: 2022-28-3
>URL:https://gov.proofofhumanity.id/t/phase-2-hip-41-allow-verbal-confirmation-for-registrating-users/1888

## Simple Summary

This would add the option to have a user, instead of holding a sign with their address, give a verbal confirmation of their public address. Either visual or verbal confirmation would be accepted.

## Abstract


The user, when onboarding, should be able to decide either to make a visual or verbal confirmation (or both) of their public address during their video. 

The current rules for profile submission require a mandatory sign (can be a screen) showing the full Ethereum address. This has been a point of failure for many people. Although many efforts where made to help resolve those problems, such as HIP-27 allowing for one character mistakes, the sign itself is just one more step to fight deep-fakes. Considering all those facts, we believe that it's feasible to replace that sign with a verbal confirmation. Instead of showing a sign with the ETH address the submitter would have to say out loud a series of words that confirm ownership of both address and media files.

## Motivation

The advantages are clear:

Easier flow, as the user can do all the process in one take in the video by following simple instructions on screen
No props needed. Human doesn’t need to fish around to get a pen and a paper or find a second screen, nor spend a long time trying to slowly copy the address.
More accessible. For people with movement or vision impairment, this would make it easier for them to be included in the system
DOESN’T EXCLUDE SIGNS: users who still prefer to hold signs (maybe someone who is speech impaired, or just shy) can still use visual confirmation of their address.

## Implementation


**BIP 039 words**

The user must look at the camera and say (in one of the officially acepted languages): 
"I certify that I am a real human and that I am not already in this registry. My identifier is "

Following by an identifier which is obtained by converting the hexadecimal ethereum address into base 2048, then converting those digits into [the official BIP039 dictionary words](https://github.com/bitcoin/bips/blob/master/bip-0039/bip-0039-wordlists.md). The user then must speak the **first 6 resulting words in the same same language as the phrase**.
> 
> Example:
> The address **0x17a91203a9e9c3519c2f76210497ef7f4be2352f**
> Would be spoken as: **Able Barrel, Debris Siege, Pretty Inquiry.** (commas and spacing are optional)

The phrase derived from the address would be generated **automatically** in the **DAPP UI**. Also it would be shown on every profile that chose this verification method, so that validators can still curate the list as usual. 

The BIP039 dictionary **MUST** be in the same language as the rest of the phrase, so when a future HIP approves a new language, this HIP will not need to be updated. If a future HIP approves a new official Proof of Humanity language that does not have an official BIP039 dictionary yet, then the HIP that adds the new language must also define an official word dictionary for the purposes of this HIP.
