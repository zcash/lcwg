# Light Client Working Group Devs Meeting 69
### Meeting Date/Time: Thursday, January 25th, 2024 17:00 UTC
### Meeting Duration: 40 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Kris (ECC), John (ZF), Danyul (Chainsafe), Zancas (Zingo), Gygaxis (Zingo), Conrado (ZF), Paul (Edge), Harry Halpin (Nym)


## Agenda:
- Team quick updates 
- Update on Binance Exchange Addresses
- Request for input: Preferred approach on ZIP-320
- Workgroup Initiatives:
  - ZIP-320 implementation across the ecosystem
  - ZIP-315 finalization and support across the wallet ecosystem: 
  - Implementation of ZIP-317 across the ecosystem:
  - Lightwalletd maintenance and support ZIP-307 / Decentralize Core development

Where? Zoom! https://zfnd-org.zoom.us/j/84957460378

### Presentation Slot: (optional)
None requested.

### Team Updates: 2-3 minute updates per team. Shorter is better
  - Kinds of team updates:
    - General Status 
    - Request for input
    - Announcements
    - Blockers or dependencies with other teams

#### Pacu ZCWD
Completed the last milestone for a past grant and filed a new grant that is pending revision and further evaluation.

Did a work on ZIP-315 review. 

#### ECC:
PRs up for transaction requests for iOS and Android
Working on orchard support. There are no public API changes affecting clients
There will be an update to Rust version support because there was an issue with


#### ZF:
Adding socks comm to FROST demo

#### Edge
Request for input on status for Detection Keys development. 

Kris: Detection keys are pretty interesting, but they require further resources for research and development. They will probably be a topic during Zeebot, since all the proposals in-flight should be prioritized and then planned. There’s a related topic on Anchor selection will play a significant role in spendabilty of funds. Background sync is actually in the works to make foreground syncing less of a burden.

Pacu: It has to be noted that background sync shouldn’t be relied on because of it being a black box

Kris: It has been tested in practice to work well.

Paul: there is no guarantee of getting more than 30 seconds per day unless the operating system considers that the app provides value for the user to grant the app more time. Also it does not work well on hybrid apps. Webviews don’t start up in background calls. Also Spend before sync has been sort of anecdotal for Edge and there haven’t been noticed major improvements in performance.

Kris: 
Request for input: syncing information from Application developers.

John: Hahn’s warp sync crate has metrics.

Kris: enumerated reasons they chose not to adopt warp sync. Warp sync tracks more witnesses than Spend Before Sync which is a problem for larger wallets (exchanges).

Paul: Considering the “past three years”  mobile devices, is computation a bottleneck?

Kris: It totally is.

Paul: are there specific targets to benchmark performance on specific mobile phones as certain viewing keys were being targeted when developing the sync enhancements.

#### Harry Halpin (Nym)
Asked about the stability of the Go code of lightwalletd and if it be maintained because they wanted to integrate Nym to that codebase first.



### META: What’s LCWG Role in terms of the Binance or other CEXs potentially Delisting ZEC? 

Kris: Hahn idea is feasible and it requires no changes to the protocol. This is a stopgap measure but we should consider solving the root cause of it that is the ability to refuse funds. We may want to change the UA encoding to actually accommodate the functionality.

Pacu: the UA would cover the functionality they are demanding and wallets not supporting this new encoding would fail. Would Binance have to support UAs?

Kris: yes but only generation. If they want to support sending to UA would be great 

Hahn offered to write a javascript library for the tex addresses so actually a UA parsing one could be written instead. 


Paul: Is there a UA parsing spec that can be implemented in Javascript? 

Kris:  yes, zcash_address crate is actually a Rust implementation of it. 

Paul: will try to get someone to develop it (no promises)

Kris: links to that
https://github.com/zcash/librustzcash/tree/main/components/zcash_address
https://zips.z.cash/zip-0316


### Workgroup’s initiatives
- Workgroup Initiatives:
  - ZIP-320 implementation across the ecosystem
  - ZIP-315 finalization and support across the wallet ecosystem: 
	- is being put in a second priority because of ZIP-320
  - Implementation of ZIP-317 across the ecosystem:
	- no updates
 - Lightwalletd maintenance and support ZIP-307 / Decentralize Core development
  - Zingo could start developing a rust version of lightwalletd and darksidewalletd. 
