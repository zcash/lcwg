# Light Client Working Group Devs Meeting 47
### Meeting Date/Time: Thursday, April 6th, 2023 17:00 UTC
### Meeting Duration: 45 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Lux (Zingo), Lost Lost (Zingo), Oscar Pepper(Zingo), John (ZF), Adi (Nighthawk), Matt (Nighthawk), Nick (ECC), Carter (ECC), Kris (ECC)
### Notes: Pacu & Adi

# 1. General Notes
* ECC Updates:
  - New APIs for Synchronizer on iOS
  - Android efforts to reduce disk space usage, number of networking and internal improvements, bring significant API changes coming in the coming months, but planned changes in the immediate future
  - Shifting the limited resources to the SDK work
  - Both platforms: better communication of current sync status APIs
  - Secant: Mostly complete for the new scope, won’t be developed further until DAGsync is implemented, App has remote config and troubleshooting and logging for internal use, % progress update will be deprecated with focus on more accurate block number sync progress.
  - Pacu: building documentation and SDK towards DAGSync, Add request for documentation if anything is not clear or missing
  - Kris: discussed the DAGSync change mechanism https://github.com/zcash/librustzcash/blob/main/zcash_client_backend/src/data_api/wallet.rs#L386-L395

* ZIP-317:
  - Zingo labs: haven’t started to implement ZIP-317
  - Are there any blockers or gaps missing?
  - Lux thinks that there is a Fee determination code that needs to be done, but according to Kris Nuttycombe, there are building blocks on librustzcash that could help.
  - Nuttycom shared these links as relevant pieces that Zingo could use to adapt to plug into most of the Fee stuff ECC has developed.
  - https://github.com/zcash/librustzcash/blob/main/zcash_client_backend/src/fees.rs
  - https://github.com/zcash/librustzcash/blob/main/zcash_client_backend/src/fees/zip317.rs
  - https://github.com/zcash/librustzcash/blob/main/zcash_client_backend/src/data_api/wallet/input_selection.rs
  - https://github.com/zcash/librustzcash/blob/main/zcash_client_backend/src/data_api/wallet.rs#L386-L395
  - Is blaze sync modularized so that an additional algorithm could be added (such as DAGsync)
  - Lux thinks the primitives are pretty baked into their codebase but they would be interested in modularizing it at least to incorporate Shardtrees.

* Nighthawk updates:
  - Planned change of minimum API levels for Android (25 at least or higher) and iOS 16 to accommodate latest security updates, Adopting the secant-based TCA arch and jetpack compose for Android
  - ECC: Android API 24 will go to 27, need to evaluate the consequence of updating to API 27, iOS 16 target.

* Parking lot questions:
  - ARM 32 testing questions: Oscar brought it up because they are trying to test this architecture, what are the testing setups being used? Are these virtual or real devices?
  - Carter shared Test Lab setup https://github.com/zcash/zcash-android-wallet-sdk/blob/main/.github/workflows/pull-request.yml
  - Incremental Merkle Tree questions:
  - How close to readiness is the crate?
  - The shard tree crate has not been formally released publicly because of other formalities that are not related to the implementation work but it’s fairly usable.

## Attendees
* Lux (Zingo)
* Lost Lost (Zingo)
* Oscar Pepper(Zingo)
* John (ZF)
* Adi (Nighthawk)
* Matt (Nighthawk)
* Nick (ECC)
* Carter (ECC)
* Kris (ECC)
