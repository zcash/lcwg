# Light Client Working Group Devs Meeting 43
### Meeting Date/Time: Thursday, February 9th, 2023 17:00 UTC
### Meeting Duration: 30 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Adi @nighthawk24, Carter @ccjernigan, Kris @nuttycom, Nick Takacs, Matthew Watt @tw0po1nt, Bobloblaw Zingo Labs, Lux Zingo Labs, John ZF, Nate ECC
### Notes: Adi

# 1. General Notes
* General
 - zcashd v5.5.0 and lightwalletd updates will follow with feature targets to support DAGSync related changes and ZIP-317
 * Android SDK
  - New SDK deployed this week
  - Internal changes to decouple GRPC from the public API
  - No major API changes
  - Android API minimum version bump to 24
  - New change in the pipeline - expand the public API to help manage SDK synchronizer and enable background sync
  - Addition of a new module as a library to be an incubator for experimental APIs
  - Bugfix: not fetching all transparent addresses and balances - android was fetching the balaces from the default T-address and not the legacy T-address. The fix might require rescanning from the last good block range scanned to fetch the balances for the legacy T-address.
* iOS SDK
  - Released ZcashLightClientKit 0.18.0 and subsequent 0.18.1 that adds a function 
  - 0.18.0 move away from custom queries for Wallet history and start using librustzcash methods directly
  - 0.17.5 has an update for fixing Xcode compile issue to follow conventions
  - Focus on 0.19.0 will include fixes file system cache and improved performance with memory management and threading
* Librustzcash
  - Work in progress to get orchard tx builder finished
  - Sparse Merkel tree for note commitments is in review, will enable lightwalletd to send intermediate note commitments to get latest blocks of transactions and have the ability to spend the notes immediately.

## Attendees
* @Pacu ECC
* @ccjernigan ECC
* Kris @nuttycom ECC
* Nick Takacs ECC
* Nate ECC
* @nighthawk24 Nighthawk
* @tw0po1nt Nighthawk
* Bobloblaw Zingo Labs
* Lux Zingo Labs
* John ZF