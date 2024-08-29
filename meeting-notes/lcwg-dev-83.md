# Light Client Working Group Devs Meeting 83
### Meeting Date/Time: Thursday, August 22nd, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Conrado (ZF), Kris, Eric & Willem (chainsafe), Fluidvanadium (Zingo), Andrea (ECC), Arya (ZF)

### Agenda

Team Updates
Problems with transactions being rejected and not getting to the “mempool” in Zebra 1.8.0 
TEX Address support status
Follow up of previous calls to action 
Getrawtransaction issues 
https://github.com/zcash/lightwalletd/issues/493
https://github.com/ZcashFoundation/zebra/issues/8744


### Team Updates
Chainsafe: 
starting to look at librustzcash wallet traits. They see a lot of influence between the sqlite and the backend.
Working on an In Memory wallet and branching off from Kris’ PR 

### Zcashd deprecation
ChainSafe could actually take on the InMemory Wallet task https://github.com/zcash/librustzcash/issues/1414 if ECC developers agree that there’s strategic value in them overseeing the development.

### problems with Zebra 1.8.0 
There’s a branch fixing the problem on Zebra and a [lightwalletd issue being worked on by ECC](https://github.com/zcash/lightwalletd/issues/497)

### TEX address Status
Android and iOS SDK releases include TEX address support and EDGE and others should be able to upgrade to the latest version of the SDKs
https://github.com/Electric-Coin-Company/zcash-swift-wallet-sdk/releases/tag/2.2.1
[Android SDK deployment](https://github.com/Electric-Coin-Company/zcash-android-wallet-sdk/commit/a4550c24a598dd0088aef77ff17f6b0892e44418)
