# HIP-36 [Phase2][Signalling]: Registration Validity Extension and Change of Renewal Period
HIP: 36
title: Registration Validity Extension and Change of Renewal Period
author: @senryu @NingFid
status: Phase 2
created: 2022-01-26

 
Simple Summary

The validity of a registered profile is 1 year. This proposal aims to extend the duration of each profile to 2 years and change the renewal period duration to 3 months.
 
Abstract

To prevent high attrition in the registry due to renewal cost and simultaneous $UBI sell-off to fund renewal, we propose a change on the validity of the registered profiles through a change of the parameter submissionDuration to 2 years. 
Moreover, the current setup to remove registered profiles is halted for the entire renewal duration of 6 months which is too long of ‘immunity’ period for possibly missed non-conforming and/or suspicious profiles. Another issue that was brought up is for those who wish to be removed but cannot initiate it(no option)until the 6-month renewal period is over. This can be done through a parameter change of renewalPeriodDuration to 3 months.
 
 
Motivation

In order for the Proof of Humanity protocol to maintain the momentum in registration and remain as the largest on-chain identity system, we need to address the pain points in submission primarily the total cost to register and renew. 
 
While the ETH usd value halved since Phase 1, ETH price forecast remains positive in the long term due to Ethereum’s widespread use (https://cryptofees.info/; https://money-movers.info/; ) and net issuance (https://watchtheburn.com/insights) relatively lower than the burned ETH from fees as of today. Might sound more speculative than concrete motivation to push this proposal through, but the Proof of Humanity registration being denominated in ETH is significantly affected by price changes.

Moreover, there are few other preceding profile submission requirement alterations being proposed HIP-32 https://gov.proofofhumanity.id/t/phase-2-hip-32-define-text-to-be-read-for-profile-renewal/1157 HIP 33 https://gov.proofofhumanity.id/t/phase-1-hip-33-registry-protection-against-puppet-and-farming-attacks/1357/2
HIP 27 https://gov.proofofhumanity.id/t/phase-2-hip-27-allow-1-character-mistakes-in-displayed-address-updated/1275
that are yet to be implemented and may be enforced at the same time as many profiles need renewing. We need more time to re-educate users and curators of the new process as we strive to balance fair incentivization and high-quality curated sybil-proof list of humans.
 
Specification

The proposed parameter changes on submissionDuration and renewalPeriodDuration will affect profiles:
- About to expire after 1 year in the registry
- Have renewed prior to the change and will have the new validity as specified in the change
- Current registrants not in renewal period
- Incoming submissions
 
Discussions found in the threads:
https://gov.proofofhumanity.id/t/extending-the-registration-period-with-one-year/1316?u=ningfid
https://gov.proofofhumanity.id/t/phase-1-hip-36-extending-the-registration-period-to-avoid-gas-costs/1538?u=ningfid
 
