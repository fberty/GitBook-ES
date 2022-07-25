# HIP-38 [Phase 2][Signaling]: Election of Proposers
    HIP: 38
    title: Election of Proposers
    author: @ludoviko, @juanumusic, 0xjean.eth
    status: Phase 2
    created: 2022-01-26

## Simple summary

This HIP establishes that the addresses gathered from the Snapshot poll (later deleted by Snapshot admins but still retrievable through other means) is a legitimate list of candidates for the proposer role, and to establish the addresses of that list should be instated as the initial seed of proposers in the Snapshot platform.

## Abstract

HIP-34 established that “Proposers” are comprised of “People elected as proposer through a proposal” (apart from Mission Board Members and others).

This proposal aims to elect the first batch of proposers. A poll made on Snapshot was used to gather a list of addresses of people interested in having that role.

## Motivation

Original and deleted proposal was in this link: [Snapshot](https://snapshot.org/#/poh.eth/proposal/0x32a19b0132c8e2e6c19bf3cd74138416f9a5f780e672a58982d00cbd827813f9). This is the IPFS link for the proposal (that does not contain the votes): https://ipfs.fleek.co/ipfs/QmbDBvUJNhyaWUu1nhGPSEpuCxqhWP9hwC2FdQuJNM1tVY

As an alternative, this is the IPFS of signed votes for proposers: https://ipfs.io/ipfs/QmYwumh4oS8N6iUvqEEhsJZkaN2DY7dfkcvrNRttzAoUTP?filename=ipfs_signed_proposors.txt. This list was provided by Laurent Genoud, developer and admin of the official Snapshot Telegram group ([Telegram: Contact @snapshotlabs](https://t.me/snapshotlabs/7972)).

The poll was used in order to guarantee that proposers belonged to the registry. There was only one option “I offer myself as Proposer”. This document [Votes poh.eth WITH LINK - Google Sheets ](https://docs.google.com/spreadsheets/d/1vsIaSvo6ee4A9HBNpG3QALE-YlDXYM6yjlskvavwsCo/edit?usp=sharing) has the IPFS links which show which people voted that option, so they voted in clear knowledge that they offered themselves as proposers.

## Implementation

Use the addresses on the list below to grant them the ability to post proposals in the PoH Snapshot pages. (IPFS copy: [https://ipfs.io/ipfs/Qmf8Nwezy1gpbtctdHtFPPJFezT6euFcCu5QFUrQYYVu3C?filename=proposoooooooooooooooors.txt](https://ipfs.io/ipfs/Qmf8Nwezy1gpbtctdHtFPPJFezT6euFcCu5QFUrQYYVu3C?filename=proposoooooooooooooooors.txt) )

List:

    0x3BE28A28B85c36FB74e513898bC11260Ee541AAC
    0xDA35c8e464889bA2Cb91d2E85C608a99D262d5db
    bobjiang.eth
    0xbeeb01a1E47450479c99b7Eb545D090cDdD78776
    0x9d9E26932d012b2Ab21B974fE1552F4025b1e1Cc
    poweroverwhelming.eth
    18183.eth
    0x6Ed3755141cecB387FCB2Ad18b537bc7F2bD524b
    0xkafo.eth
    0x31452B884F5269eD21e2BAB44CC6A9d48eAac85f
    0x6E9A88971e957Abb41bAe4E2677caE258F0c1e76
    zrowgz.eth
    bosco.eth
    0xe724C1D534284f2837F3ab310eF8329BBD7c045E
    0xae55D42e157E35a075BA38De7E871178648D2d30
    0x342f5be7578CA67506a31214D93a99e5504256CC
    0x5886f65425cad457776d7a89a399907c97e608e5
    0x85c2043C36be1b84A789E92c29ee3e918ddF50f4
    0x275203A89ACEEdee0D07aF626830baE536b36eD1
    erik.bjareholt.eth
    0xcBCA1f03D67472A7bEe257798Fc93c7eC6c5BE77
    0x96925d8E33AE06F6fC9F185F106C6F026d36B352
    0xBfF6800aF73a36a7b1821Cc9f18DB00cA4Aa4b3d
    0xb0CC32190a06f4bA13027E7D6C516217b49E8eb0
    0xe17aE4Ee9f37524d2a25177C8a6C95e51DD85262
    0x6bFadF56F24583A777020F6B6EEb11591D79270c
    0xcdf2bc5eAE545953A840457eCDCd5a5Bd4466f66
    0xb8F6b7dfCA935D1aDB58ab18177F5B72a939Ba70
    0x87EE3c1Fb15eae5b9965493C2020dbd3AdACdAfA
    0x87EE3c1Fb15eae5b9965493C2020dbd3AdACdAfA
    0xcb68A8138c1e57691574670f435A36dB5eCC8E2a
    0x39Df2B98daDA52248309770B530c2D2ED0908Cd3
    0x670F6eFC8DBA20BBb1BF49bad31845e47216BFF9
    0x6c97785edAf8f949a353fcc1629d48759B12F323
    0x6c97785edAf8f949a353fcc1629d48759B12F323
    0xc0086412BA221bd43e69852c9eA38336D6310885
    0xe17aE4Ee9f37524d2a25177C8a6C95e51DD85262
    0x7b694B2a461E58b0673565fB8B1D83E962Ed70f3
    dacastillo.eth
    charles53300.sismo.eth
    0xC17671afEc156398D65ffCBD37ea2B3C12225684
    0xC17671afEc156398D65ffCBD37ea2B3C12225684
    shotaro.eth
    0xA72ef9BB82d59464eAA63f461C273f8028b20f5c
    0xa697c106f153ba7Fa3801bA2afd6273559c7b105
    0x6E9A88971e957Abb41bAe4E2677caE258F0c1e76
    0x6E9A88971e957Abb41bAe4E2677caE258F0c1e76
    0x364144a07f23EF285DF585D3E4239Ca7B1102535
    0xcd3c6214dd023eEA574410FfF03d3c065dc560F3
    nicobilinkis.eth
    0xE30827AE68533e7a01Fb8369d5219f18D5f70e87
    0x3BE28A28B85c36FB74e513898bC11260Ee541AAC
    matiasben.eth
    jfdominguez.eth
    0x8BF7Cd4aE85F765a06006802e21bbCC968f45421
    0x14f284988198bBD305C44b7BEA8748323fBB8419
    0x0827ED3a46c9793005e4D68E838DE577Cd8DD752
    0xb3ca2de6af06BF736c609F3e4dD1307570a37732
    0xb3ca2de6af06BF736c609F3e4dD1307570a37732
    0x5CfA0c362DADEa86478d05767ed800dd1B026749
    0x26D06ec9a2dd19cb33398a58f75d9Aa61dda11cD
    v4len.eth
    0x61E067aF897a0a9130e5Fbb9bF089223FCa10820
    0x6F772F596bB0e9e534Ac99D782eE36578dd15B14
    drlorente97.eth
    ludoviko.eth
    0xmanu.eth
    juanu.eth
    0xjean.eth
