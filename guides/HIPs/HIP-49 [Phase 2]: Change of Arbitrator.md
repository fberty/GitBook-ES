# HIP-49 [Phase 2]: Change of Arbitrator
```
HIP: 49
title: Change of Arbitrator
authors: MoniK, HBesso31.eth, pCorace.eth, nicobilinkis.eth, castorpolux.eth, Roberto Iquitos, Andres Vilches, Ruben Alejandro Puca Vilte, drlorente97.eth,  jfdominguez.eth, Pablo Buencrypto, ANM, Flor Velastiqui, Hernán DLF, lautaro.eth, juanipose.eth
status: Phase-2
created: 2022-07-05
```

### Simple Summary

The goal of this proposal is to change the smart contract that deals with disputes to the profile submission and removals (a.k.a, the Arbitrator) with a new one that serves better the interests of the Proof of Humanity community.

### Abstract

The Proof of Humanity contract will change its arbitrator to a new deployment of a [Kleros Arbitrator](https://github.com/kleros/kleros) that will be an exact replica of the existing one but with one critical chage:

* The Governor of the new contract will be set to the Proof of Humanity Governor address (`0x327a29fcE0a6490E4236240Be176dAA282EcCfdF`) so future changes around Proof of Humanity's dispute resolution court are set by its own community as well.

This new arbitrator will also be set on the Governor Contract (`0x327a29fcE0a6490E4236240Be176dAA282EcCfdF`) of Proof of Humanity, effectively putting any potential disputes that happen with it on the hands of the Proof of Humanity DAO.

Everything else will remain exactly the same in order to guarantee compatibility with the road tested settings of past dispute resolutions. The tokenomics of the new Arbitrator will not be modified with neither UBI nor an alternative new token. **PNK will remain as the only staking token valid for this new arbitrator.** 

### Motivation

The Kleros Arbitration smart contracts that are being used by the Proof of Humanity protocol and the Proof of Humanity DAO are currently governed by the Kleros Coop where they are the only entity that can define its parameters moving forward. 

Our aim is to further decentralize the Proof of Humanity project by using the democratic processes put in place by the Proof of Humanity DAO. During the first year of our DAO, not a single election has been disputed with over 40 decisions being made by the DAO and the combination of Proof of Humanity with Snapshot has proven to be an efficient approach to democratic decision making. 

Our goal is to use this mechanism to decide over the Arbitrator being used by the Protocol and the DAO's Governor contract.


### Specification

Any potential dispute that emerges today either from the Proof of Humanity Governor or the Proof of Humanity DAO will go to an Arbitrator contract that ultimately has its parameters set by the Kleros Coop.

A comparison between the vote distribution in the decision making process between the Proof of Humanity DAO and the Kleros Coop show very different distribution of power on each organization:

![Proof of Humanity DAO](https://gov.proofofhumanity.id/uploads/default/original/1X/e65fa8189d1f22457c13cbd8bfd22a10fd06ea66.jpeg)

![Kleros Coop](https://gov.proofofhumanity.id/uploads/default/original/1X/c3e9c0fe4800da1c99aa086bece58d04b610e43a.jpeg)

As much as we trust the knowledge and experience that Kleros has contributed to the Proof of Humanity project, by advancing with this change the Proof of Humanity community will be able to set the rules for its own Arbitration mechanisms and take an effective step towards greater decentralization.

**No project ever begins decentralized. It's up to the community to take the necessary steps to guarantee progressive decentralization. With the approval of this proposal we are taking a critical step in that direction.**

For this purpose, we will deploy a new contract that follows the same exact settings the current Arbitrator has but with its Governor set to the Proof of Humanity Governor. And the Proof of Humanity Governor's Arbitrator will be set to the new Arbitrator being deployed.


### Rationale

The incorporation of an Arbitrator dependent of the Proof of Humanity DAO would reduce the risk of the DAO being captured in a Governance Gridlock by actors that are not aligned with the core interests of Proof of Humanity. 

This change will increase the robustness of the DAO, in accordance to a more mature decentralization since every verified human will have a right to vote over the parameters of the Arbitrator. 

Additionally, we would be able to modify the Governor with the power of *1 person 1 vote*, giving the DAO sovereign control over its own Dispute resolution courts. 

DAO control over the arbitrator and its governor is key to emancipate Proof of Humanity as an autonomous organization free from centralized interests.

With autonomy over the design of the courts we can later add after careful Tokenomics research the possibility of limiting large concentrations of staking, and incentivizing the same principles of equal access to justice within our Registry. 

Another advantage that we have over the Kleros Courts is that Humanity Court can better specify and regulate juror misconduct or exploitative behaviours in a faster, more efficient way.

Future implementations of Courts serving the Proof of Humanity protocol —whether its Kleros v2 or a new compatible Arbitator— can only be accepted if they also follow the configurations described on this HIP and thus maintain the Proof of Humanity Governor as the Arbitrator Governor. No other settings can be accepted in the case of a Court Update in the future. 

### Implementation

An exact replica of the existing Kleros arbitration contract will be deployed on Ethereum Mainnet. 

The same version of `KlerosLiquid.sol` smart contract found on Proof of Humanity's current court available on `0x988b3A538b618C7A603e1c11Ab82Cd16dbE28069` will be used.

The new court will be deployed with the following settings in its `constructor` function:

```
// The governor of the contract will be set to the Proof of Humanity governor.
address _governor = 0x327a29fcE0a6490E4236240Be176dAA282EcCfdF

// The pinakion token contract will keep using the PNK token.
Pinakion _pinakion = 0x93ed3fbe21207ec2e8f2d3c3de6e058cb73bc04d

// The random number generator contract will keep using the existing RNG.
RNG _RNGenerator = 0x1738B62E403090666687243e758b1C29eDfFc90e

// The minimum staking time.
uint _minStakingTime = 8700000000000000000000

// The maximum drawing time.
uint _maxDrawingTime = 7200

// Whether to use commit and reveal or not.
bool _hiddenVotes = false

// Minimum tokens needed to stake in the court.
uint _minStake = 8700000000000000000000

// Basis point of tokens that are lost when incoherent.
uint _alpha = 5000

// Arbitration fee paid per juror.
uint _feeForJuror = 25000000000000000

uint _jurorsForCourtJump = 31

// The time allotted to each dispute period in the form `timesPerPeriod[period]`.
uint[4] _timesPerPeriod = [540000, 437400, 437400, 291600]

// The number of children per node of the general court's sortition sum tree.
uint _sortitionSumTreeK = 8

```

Once this contract has been successfully deployed on mainnet, it will be set to have a Court with ID 1 that will work as the Humanity Court that will be linked to Proof of Humanity. 

Then the following tickets will be submitted to the Proof of Humanity Governor:

- *HIP 49 Change the Arbitrator of the Proof of Humanity Protocol*: The Proof of Humanity protocol (`0xC5E9dDebb09Cd64DfaCab4011A0D5cEDaf7c9BDb`) will execute `changeArbitrator` with the paremeter `address _arbitrator` set with the new arbitrator contract and the extra bytes data necessary to connect it to the Humanity Court with Court Id 1. 
- *HIP 49 Change the Arbitrator of the Proof of Humanity Governor*: The Proof of Humanity Governor (`0x327a29fcE0a6490E4236240Be176dAA282EcCfdF`) will execute `changeArbitrator` with the paremeter `address _arbitrator` set with the new arbitrator contract and the extra bytes data necessary to connect it to the Humanity Court with the Court Id 1. 

Once these changes are in place, the Proof of Humanity DAO will effectively control the rules of its own Arbitrator and disputes on the Governor will be setlled by the Proof of Humanity Arbitrator contract. 
