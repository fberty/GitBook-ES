# HIP-1: UBI Accrual Rate based on Vouching Activity.
Forum discussion: https://gov.proofofhumanity.id/t/hip-1-ubi-accrual-rate-based-on-vouching-activity/128

The accrual rate of UBI can be connected to the activity aimed at growing the Proof of Humanity network. Users that are spending gas to vouch for other humans, will be rewarded with more UBI than those that are not contributing to the growth of Proof of Humanity.

Taking into consideration that the current accrual rate is `0.00028 UBI per second` (or `1.00 UBI per hour`), users will be able to earn the full rate if they vouch for at least one human in Proof of Humanity. If a user has never vouched for someone, she can still accrue UBI but at a fraction of the full accrual rate. We suggest to lower the accrual to 1/10th the rate (ie. `0.10 UBI per hour`).

# Development

The UBI token contract will be upgraded with a new interface to Proof of Humanity that will have the ability to call `getSubmissionInfo` and obtain for a given address if it has vouched or not for someone else using the `hasVouched` boolean value returned by Proof of Humanity. 

```
interface IProofOfHumanity {
  function isRegistered(address _submissionID)
    external
    view
    returns (
      bool registered
    );
   function getSubmissionInfo(address _submissionID)
     external
     view
     returns (
       bool status,
       uint submissionTime, 
       uint index, 
       bool registered, 
       bool hasVouched, // value used for accrual rate
       uint numberOfRequests
     )
}
```

The `getAccruedValue` function  that is called by `balanceOf` will then take into consideration if a given address has vouched or not and set the accrual rate based on this data.

# Considerations

This will mitigate inflation of the UBI token during its initial phase and reward participants in the network that are effectively contributing to its growth.

Users that have accrued UBI before this modification will have to transfer their funds to a new address to keep their accrued UBI, or else their accrued UBI so far will be impacted by the new formula if they haven't vouched for anyone yet.
