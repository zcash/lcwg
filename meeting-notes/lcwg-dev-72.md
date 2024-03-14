# Light Client Working Group Devs Meeting 72
### Meeting Date/Time: Thursday, March 7th, 2024, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Pili (ZF), Andrea (ECC), Daira-Emma (ECC), Paul (EDGE), William (EDGE), Matthew (EDGE), Conrado (ZF), Jason McGee (ZCG), Eric Tu (Chainsafe), Rene (Zenith), Zancas (Zingo)


## Agenda:
- Quick team updates 
- ECC mobile SDK deployment frictions for React Native (E.g: EDGE)
 - Timing of Android and iOS releases
 - Cocoapods Support
- Discussion: development, outreach and deployment of Binance "transparent-source only t-addresses" and ZIP-320 implementation across the ecosystem

## Quick updates:

ECC:
Will be rolling out support for ZIP-320 the SDK the following week

ZINGO: 
Working on adding regtest mode on Zebra.

ZF:
Will start working with Zingo on regtest mode next week

Chainsafe:
Been working on a feasibility test on Zcash Javascript SDK. Will post detailed information on progress in the forums during the week

Rene: 
Working on Zenith full node wallet. no blockers.

## ECC mobile SDK deployment frictions for React Native (E.g: EDGE)
Edge coded a script to extract the swift packages of ZcashLightClient and zcash-light-client-ff and re-bundle them into a cocoapod. 

Str4d is working on solving a build problem that allows to unify the ffi and Zcash iOS SDK into one repo again and have a build system that allows developers to choose to either build from source or using a built rust artifact without having two repos.

Problems of embedding rust back into the SDK:
- Build time
- need to have rust on the system to use the package

Problems of having separate repos:
- Artifact sizes
- Rust developer experience decays

Str4d’s intention is to thread the needle so that:
- Tagged releases can have built artifacts (developers that are clients of the sdk)
- Commits would build from source using the rust toolchain (sdk developers)

This is being discussed here: https://github.com/Electric-Coin-Company/zcash-light-client-ffi/issues/96

Ideally this will get worked on after Zashi 1.0 is released


## ZIP-320 deployment on the SDKs and clients.
EDGE requests that there is a snapshot release of ZIP-320 for iOS and Android for them to work on before the end of march to accommodate some scheduling of their team. Also for production, EDGE would need both Android and iOS to be available at the same time so they can release a new version of their react native Zcash component.

The next release of the SDKs will include changes on their APIs to return more than one transaction when TX is proposed, because TEX addresses can return more than one transaction. 

The new API will replace the old ones once TEX address support is rolled out (in about three weeks)

The new APIs will return a Flow (android) or AsyncThrowableStream (Swift) of transaction results. 

