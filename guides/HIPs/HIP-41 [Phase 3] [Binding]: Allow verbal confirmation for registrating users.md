# HIP-41 [Phase 3] [Binding]: Allow verbal confirmation for registrating users
>HIP 41
>Title: Allow verbal confirmation for registrating users
>authors: avsa.eth and nicobilinkis.eth
>Status: Phase 3
>Created: 2022-28-3

[Gov forum post](https://gov.proofofhumanity.id/t/phase-3-binding-hip-41-allow-verbal-confirmation-for-registrating-users/1975)

# Simple Summary
This would add the option to have a user, instead of holding a sign with their address, give a verbal confirmation of their public address. Either visual or verbal confirmation would be accepted.


# Abstract
The user, when onboarding, should be able to decide either to make a visual or verbal confirmation (or both) of their public address during their video. 

The current rules for profile submission require a mandatory sign (can be a screen) showing the full Ethereum address. This has been a point of failure for many people. Although many efforts where made to help resolve those problems, such as HIP-27 allowing for one character mistakes, the sign itself is just one more step to fight deep-fakes. 
Considering all those facts, we believe that it's feasible to replace that sign with a verbal confirmation. Instead of showing a sign with the ETH address the submitter would have to say out loud **8 words** that confirm ownership of both address and media files.

# Motivation
The advantages are clear:

* Easier flow, as the user can do all the process in one take in the video by following simple instructions on screen
* No props needed: Human doesn’t need to fish around to get a pen and a paper or find a second screen, nor spend a long time trying to slowly copy the address.
* More accessible: For people with movement or vision impairment, this would make it easier for them to be included in the system
* DOESN’T EXCLUDE SIGNS: users who still prefer to hold signs (maybe someone who is speech impaired, or just shy) can still use visual confirmation of their address.

# Implementation

## Changes to the primary document
Modify section 4 of the primary document to the following:
> 4. Video of the submitter - Required
> * **The user can choose to display his Ethereum address using a physical sign. 
The sign has to display in a readable manner the full Ethereum address of the
submitter (No ENS; no ellipsis). The sign can be a screen. The submitter must
show the sign in the right orientation to be read on the video.**
    A single one of the following errors occurring once will be tolerated in the displayed address:
    - omitted character: a character is omitted from the address (e.g. “abcd” →
    “abd”).
    - mistaken character: a different character has been written in place of the
    one expected in that position (e.g. “abcd” → “ab9d”).
    - swapped adjacent characters: two characters adjacent to each other have
    been swapped (e.g. “abcd” → “acbd”, but not “adcb”).
    - additional character: an additional character has been inserted anywhere
    in the address (e.g. “abcd” → “abc0d”).

> * **The user can choose to use verbal confirmation. The user has to say the 8 words that are shown on the screen when recording their video. These words are the result of turning the submitter's Ethereum address into base 2048 and then matching these with the BIP-039 dictionary of the same language that the user is using for the rest of the phrase. Word omission or order swapping are not allowed. Poor accents or mispronunciations are not grounds for rejections. The verbal confirmation must be said in the same language as the rest of the phrase.**
> * The submitter must say « I certify that I am a real human and that I am not
already registered in this registry ». Submitters should speak in their normal voice
and should not attempt mimicking someone else’s voice. Speaking before or after
the required sentence is acceptable. Poor English accents, mispronunciations,
and the switch or oversight of words in that sentence are not grounds for
rejections.
> * Video submissions must follow all of the following requirements:
    * at most 2 minutes long,
    * in the video/webm, video/MP4, video/avi or video/mov format,
    * vertical (portrait), horizontal (landscape) or square,
    and follow these minimum size requirements:
    * Minimum height: equal to or higher than 352 pixels
    * Minimum width: equal to or higher than 352 pixels
> * Lighting conditions and recording device quality should be sufficient to discern
facial features and characters composing the Ethereum address displayed.
> * The quality of the audio should be high enough such that the speaker can be
understood clearly. Small background noises are acceptable as long as they
don’t prevent a clear understanding of the speaker.
> * The face of the submitter should follow the requirements of section 2





**BIP-039 words**

The user must look at the camera and say (in one of the officially accepted languages): 
"I certify that I am a real human and that I am not already registered in this registry. My confirmation phrase is "

Following by an identifier which is obtained by converting the hexadecimal Ethereum address into base 2048, then converting those digits into [the official BIP-039 dictionary words](https://github.com/bitcoin/bips/blob/master/bip-0039/bip-0039-wordlists.md). The user then must speak the **first 8 resulting words**.

The BIP039 dictionary **MUST** be in the same language as the rest of the phrase, so when a future HIP approves a new language, this HIP will not need to be updated. If a future HIP approves a new official Proof of Humanity language that does not have an official BIP039 dictionary yet, then the HIP that adds the new language must also define an official word dictionary for the purposes of this HIP.
> 
> Example:
> The address **0x17a91203a9e9c3519c2f76210497ef7f4be2352f**
> Would be spoken as: **absent, tumble, catch, dentist, visual, ask, crime, control.** (commas and spacing are optional)

The phrase derived from the address would be generated **automatically** in the **DAPP UI**. Also it would be shown on every profile that chose this verification method, so that validators can still curate the list as usual. Both options can be seen in the Demo below. 

## Demo

![](https://i.imgur.com/swnEfg5.jpg)
![](https://i.imgur.com/b4LN7DZ.jpg)









