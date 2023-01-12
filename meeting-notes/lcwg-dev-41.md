# Light Client Working Group Devs Meeting 41
### Meeting Date/Time: Thursday, January 12th, 2021 17:00 UTC
### Meeting Duration: 30 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Adi @nighthawk24, Carter @ccjernigan, Kris @nuttycom, Nick Takacs, Matthew Watt @tw0po1nt, John ZF
### Notes: Adi

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| | ||


# 1. General Notes
* General
 - CI/CD Travis CI & GitHub actions. Bitrise is free for open source projects.
 - GitHub actions - possible to run locally. Can use Play Store signing key for publishing.
 - Draft PR up to accommodate binary encoding specified for unified addresses to save a few bytes.
 - ZIP-321 needs update when a URI includes UA to transparent address and a memo, then the wallet should refuse to send the transaction. Adi to create a issue.
* Android SDK
  - New SDK release v1.11.0-beta01
  - API change to v.1.12.0-beta01
  - Bunch of new code in the compose UI, some of that will be ported to the SDK
* iOS SDK
  - 0.18-beta is on the way following the fix of file system cache
  - Main change is the way blocks are downloaded, reduced number of blocks are stored. Once the filesystem has the cache, a migration function to dump the cache.
  - The built in Filemanager higher level API does not have streaming function, it has save to disk. The improvement is minimal on iOS.
  - New work on inner changes to accommodate interface changes for DAGSync. The bigger changes are the latest one and the 0.18.0
  - Dropped support for cocoa pods on v0.18.0
* Lightwalletd
  - Shardtree state PR crate is in review.
  - Stack of changes: we can begin refactoring zcashd - add note commitment tree position to the combat block format, then changes to zcashd to compute root of a subtree every 16-20 commitments (stored in cached db) - needs change of C++ implementation of incremental Merkel tree to the frontier type change, then a full history of 2^16 subtree roots can be made available to lightwalletd.
  - Approx. timeline - next week zcashd part work, then hopefully done by end of Jan, then release zcashd release for end of service height - hoping to get the zcashd changes in place.
  - Documentation of spinning up lightwalletd is not up to date, this might be causing issues with lightwalletd public infrastructure when re-orgs trigger cache clearing - maybe volume is being dropped when container restarts - reconstruction of cache may be causing the delay. Check the configuration of pointing the lightwalletd infra.
  - On client apps, check the hash of the blocks and not only block height for depending on the longest chain for accurate data.
* Nighthawk Wallet
  - Migrating to Swift Package Manager
  - Updating SDKs and accommodating changes to the codebase

## Attendees
* @Pacu ECC
* @ccjernigan ECC
* Kris @nuttycom ECC
* Nick Takacs ECC
* @nighthawk24 Nighthawk
* @tw0po1nt Nighthawk
* John ZF