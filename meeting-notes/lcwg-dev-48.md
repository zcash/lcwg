# Light Client Working Group Devs Meeting 48
### Meeting Date/Time: Thursday, April 20th, 2023 17:00 UTC
### Meeting Duration: 36 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Lux (Zingo), Mandeep (Nighthawk), John (ZF), Matt (Nighthawk), Luca Campobasso (Eiger)
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


* Nighthawk updates:
  - Android:
    - Questions regarding availability of variable fee API
    - currently working on Onboarding, seed phrase import flows as well as main flow
  - iOS:
    - currently finishing work on Onboarding, seed phrase import flows as well as main flow
    - will add no-logging-target upstream for secant iOS

* Eiger Updates:
  - Luca Campobasso is one of the developers behind https://github.com/eigerco/uniffi-zcash-lib
  - They are finishing the last items that will complete their grant milestones
  - They'd like to work with librustzcash maintainers to actually integrate the uniffi project to 
  the main project so it's everything in a single place.
  - Also seeking another grant to add Go as an available language for the uniffi layer.

* John (community support ZF):
  - John has spotted some rough edges around how some transactions are being displayed on the Zcashd wallet specifically on tx's that are to the same wallet but to different account within itself. 
  He'll gather samples and document he's impressions and contact the core team about it. Overall the issue is not affecting overall display or accuracy of balance whatsoever. 


## Attendees
* Lux (Zingo)
* Mandeep (Nighthawk), 
* John (ZF)
* Matt (Nighthawk)
* Luca Campobasso (Eiger)