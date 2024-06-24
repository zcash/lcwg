# Light Client Working Group Devs Meeting 79
### Meeting Date/Time: Thursday, June 13th, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Kris (ECC), Arya (ZF), Conrado(ZF), Jason (ZCG), John (ZF), Paul (EDGE)


## Agenda:
- Quick team updates 
- ZIP-320 updates, deployment of TEX addresses coordination
- Progress Cocoapods Support for ECC iOS SDK
- Open discussion

### ZIP-320 updates, deployment of TEX addresses coordination
Currently there’s an estimated deployment date on June 30th. There’s a problem on iOS from Apple when using XCFrameworks with Xcode 15.3 and higher. There’s no apparent solution for App Store uploads so developers should anticipate manual builds and uploads using 15.2 as the worst case scenario.

In terms of SDKs there are no API changes. That’s not the case for Rust changes that Zingo is relying on. 

PR in review for is here: https://github.com/zcash/librustzcash/pull/1257 

Zingo is working to get these changes integrated and they are targeting the following week.

Jason asked about June 30th and how close we were to locking that date. Kris and Andrea confirmed that they were absolutely hitting the date.

Paul mentioned that they have a code freeze tonight for a release in two weeks

### Misc nuances of Darkside testing.

There’s the need to actually create a way to maintain a commitment tree for darkside. 
Zingo is working on a Rust implementation of LWD that might be useful for darksidewalletd tests


### Tor integration of Zashi iOS with Arti through the FFI.
Str4d did a PoC for Tor integration for the SDK for fiat conversion data retrieval through Tor.

### Zebrad regtest support 
Zingo is advancing on this as part of the Zcashd deprecation effort

### FROST mobile
Advances were made towards using UniFFI to expose the FROST Rust SDK with swift and kotlin. This work was put aside a bit to favor Go bindings because Red Dev requested for the Avalanche Go integration with FROST for the ZavaX bridge (and ZCG approved that change of priorities).

A warning for other developers aiming to use UniFFI is that deployment of the artifacts and consolidating all the possible release cycles of the different languages is not tackled by Mozilla UniFFI.

### Hardware wallet support on mobile
Andrea didn’t have any news from the Zondax team but from what they have analyzed what Zondax has develop is no use for them to use ledger with Zashi.


Kris asked Conrado if they would be able to define a transaction plan protobuf schema to define how a transaction plan should look like. Conrado said that there could be an opportunity to do so within their next cycles of FROST work. 


Both FROST, MPC and Hardware wallets need view-only support and detaching transaction signing from transaction plan creation. 


