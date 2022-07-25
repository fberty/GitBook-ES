# HIP 27 [Phase 3] [Binding]: Allow 1-character mistakes in displayed addresses
# [Phase 3] - HIP 27: Allow 1-character mistakes in displayed addresses

https://gov.proofofhumanity.id/t/phase-2-hip-27-allow-1-character-mistakes-in-displayed-address-updated/1275

```
HIP: 27
title: Allow 1-character mistakes in displayed addresses
author: @Mizu @juanu
status: Phase 2
created: 20
```
## Simple Summary
This proposal would modify the registry policy to allow for limited mistakes or omissions in the address displayed in a profile’s video.

## Abstract
Many profiles get challenged due to mistakes affecting a single character in the address displayed by the submitter in their video. This proposal would make it so a single such mistake would no longer be grounds for rejection. This would not reduce the security of the profile or the PoH registry in any practical terms as will be demonstrated below.
Motivation

Submitters will often write down their address by hand instead of printing it or displaying it on another screen. This might be because they don’t have a printer or another device with a screen they can easily display it on, or simply because they find writing the address by hand to be more convenient at that time.

As one might expect, it is often the case that submitters make mistakes when copying their address. Sometimes, these are significant errors such as the omission of a large part of the address, in which case it might be possible for an attacker to generate matching addresses, but often the error will affect only one character. We may distinguish 4 types of errors:

```
- omitted character: a character is omitted from the address (e.g. “abcd” → “abd”)
- mistaken character: a different character has been written in place of the one expected in that position (e.g. “abcd” → “ab9d”)
- swapped adjacent characters: two characters adjacent to each other have been swapped (e.g. “abcd” → “acbd”)
- additional character: an additional character has been inserted anywhere in the address (e.g. “abcd” → “abc0d”)
```

This proposal would allow at most one of the above three errors in a displayed address. The effects on the security of an address (i.e. on the ability of an attacker to find a private key generating an address which would match the displayed address) would be the following:

```
- omitted character: 9.32 bits: lg(40*16): 40 positions to insert the missing character which has 16 possible values
- mistaken character: 9.23 bits: lg(40*15): 40 characters with 15 possible invalid values each
- swapped adjacent characters: 5.29 bits: lg(39): 39 possible swaps of adjacent characters, although note that this can be slightly lower still since not all swaps have an effect (e.g. in “abbd”, swapping the two "b"s has no effect)
- additional character: 5.36 bits: lg(41): 41 choices for which character to delete
```

Note that if a character is missing (case 1.) the three other cases are no longer allowed, and conversely, if the displayed address has all 40 characters (case 2. and 3.), the first and fourth cases are no longer allowed, and if there is an extra character, then only case 4. may be considered. As a result the maximum security loss is max(lg(N_1), lg(N_2 + N_3), lg(N_4)) = max(9.32, 9.32, 5.36) = 9.32 bits, reducing the total security of an address from 160 to 150.68 bits. Given the low stakes involved in being able to create a fake profile with an existing PoH registration video and the fact that no one is likely to be able to crack 150 bits of an Ethereum key for the foreseeable future, this should be an acceptable security compromise.

At this point, it is worth noting that there is one disadvantage to this proposal: It will no longer be possible to find a person’s profile from the video alone without trying all possible allowed errors, which is to say 639 trials in the worst case. This is easily remedied with a simple software loop, but something to keep in mind.

## Specification
The following text will be appended at the end of the first bullet point of subsection 4. of the “List of current required/optional elements and submission rules”:
```
A single one of the following errors occurring once will be tolerated in the displayed address:
- omitted character: a character is omitted from the address (e.g. “abcd” → “abd”)
- mistaken character: a different character has been written in place of the one expected in that position (e.g. “abcd” → “ab9d”)
- swapped adjacent characters: two characters adjacent to each other have been swapped (e.g. “abcd” → “acbd”, but not “adcb”)
- additional character: an additional character has been inserted anywhere in the address (e.g. “abcd” → “abc0d”)
```

As stated on the effects on security, 1 character does not add a great impact on security, but it does greatly impact on UX and humans registering making honest mistakes. 
It could be argued that in a future time, we could be allowing more characters mistakes, which would lead to a slippery slope. The key point is to maintain security and adding more characters would have a greater impact on security. 1 character mistakes can be considered as a good balance between honest mistakes while maintaining security.

## Mission Board Ratification
Since this HIP has been recreated from an existing phase 2, the proposers have asked the Mission Boards to ratify the validity of this HIP. The board's vote on this phase 3 is proof enough that they confirm it's validity. (See https://gov.proofofhumanity.id/t/special-binding-mission-board-ratification-hip-27/1417)
