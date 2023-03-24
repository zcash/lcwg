# Light Client Working Group Devs Meeting 46
### Meeting Date/Time: Thursday, March 23rd, 2023 17:00 UTC
### Meeting Duration: 45 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Adi @nighthawk24, Mandeep Bhalotia @Mandeepbhalothia, Carter @ccjernigan, Matthew Watt @tw0po1nt, John ZF
### Notes: Adi

# 1. General Notes
* Updates
 - Adi: working on setting up globally distributed for the updated infrastructure
 - Matt: started working on splash screen & onboarding screen with new design and planning to be additive with the changes, so easy to pull new files and contrinute changes upstream
 - Mandeep: working on adopting Jetpack Compose architecture for Android and working with existing files and setup
 - Pacu: A new project is a good opportunity to test documentation, request to raise an issue if anything is not clear. Communicate via email for long verbose issues, or small issues to fix things.
 - ECC core team has been committed to fix a block chain vulnerability affecting 100+ chains that are forks of Bitcoin codebase. Delayed by a month on other items in line with performance. On the wallet team, a lot of changes in terms of bootstrapping code infrastructure to change the SDK to make it safer.

 - iOS SDK:
  - Friendly interface and inner overhaul work to solve concurrency issues. And fix issues during runtime.
  - Working on a bunch of items: consolidating interfaces on the SDK synchronizer as async was difficult to integrate in clients that did not use async. Apple didn’t provide good tooling to reconcile those scenarios. Other events with SDK synchronizer which makes the combined and reactive approaches more in line with a closure and combined based API to be better suited with other clients that wrap the SDK to React native modules will benefit from closure based work and Swift based clients will be better suited with the combined approach.
  - Aliasing the synchronizer to keep once instance running, avoid memory leaks scenarios and eliminate those scenarios. Add support for multiple seed wallets.
  - Additional feature to convert seed words in to an identifier.
  - Secant iOS - work towards adopting new SDK changes. 

 - Android SDK
   - Working to get disk space usage relinquished. iOS clears cache to keep at most 100 blocks info.
   - Migrate Android app to the latest jetpack compose version.

 - What’s to come: Wallet developments and use cases article by @str4d https://hackmd.io/@str4d/dagsync-graph-aware-zcash-wallets


## Attendees
* @Pacu ECC
* @nighthawk24 Nighthawk
* @tw0po1nt Nighthawk
* @Mandeepbhalothia Nighthawk
* John ZF