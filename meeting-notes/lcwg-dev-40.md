# Light Client Working Group Devs Meeting 40
### Meeting Date/Time: Thursday, December 15th, 2022 17:00 UTC
### Meeting Duration: 30 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Adi @nighthawk24, Carter @ccjernigan, Kris @nuttycom, Matthew Watt @tw0po1nt, Bobloblaw Zingo Labs, Lux Zingo Labs, Oscar Zingo Labs, Daniel Wolande ZF, John ZF, Nate ECC
### Notes: Adi

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| | ||


# 1. General Notes
* General
 - Lightwalletd has major refactor coming up with DAGSync
 - First: to use as much as possible with current sync process with an updated note commitment tree, with the change to LWD add the ability to make the notes immediately spendable without waiting for the sync to complete
Second: Discussion around changes needed for Orchard support, str4d has pushed changes to make it possible

https://github.com/zcash/librustzcash/pull/734

https://github.com/zcash/incrementalmerkletree/pull/50

 - Change in LWD will be for light clients to allow plugging in to roots of the tree to make them spendable.
 - Overall improvement in usability
 - ECC had their own forks to support cashed and internal light wallet software, ECC is working towards resolving it
 - Shipping rapid releases is an impetus for working with forks.
 - LWD APIs will be backward compatible
 - Open issue on LWD for better reorg handling and maybe consider having a singling system for light wallets to tell the user of the server and wallet status.
 - Lux from Zingo Labs: Updating notes is a significant part of the sync time. Even without the immediate spending, this note commitment change will be a significant sync boost
 - Darksidewalletd is an easier approach to run integration tests.
 - LibRustZcash has a ZIP-317 implementation available.
 - It should be possible to use the types to prepare a tx with a give fee strategy, get that ready to broadcast. Expose at the FFI layer is all in one step.
 - Discussed various wallet scenarios of note commitment selection issues while the wallet is still syncing.
- "In the case that a client is confident that it is the only spend capability holder, can’t that client immediately spend given sufficiently confirmed funds?”
- “If we need to construct the transaction to determine the fees, that's a UX inconvenience, but a minor one.”
- There's a wallet-dev channel in Zcash R&D it's intended for this group

* Android SDK
  - New snapshot of 1.11 SDK with stable APIs
  - Skipped 1.10 as it is consumed within the app
  - Plan to do the release after the holidays
  - No known issues in the build
  - Branch in ECC wallet build for 1.10, working on 1.11
* iOS SDK
  - Released ZcashLightClientKit 0.17.2, 0.17.3, 0.17.4 which have bug fixes and enhancements around fetching transparent outputs
  - 0.17.4 has no pressing issues
  - Plan to release the 0.18 after the holidays which includes several updates around using the file system instead of SQLite and other enhancements like reducing the amount of blocks handled at once
  - Deleting the huge DB after reaching chain tip to free up user device memory

## Attendees
* @Pacu ECC
* @ccjernigan ECC
* Kris @nuttycom ECC
* Nate ECC
* @nighthawk24 Nighthawk
* @tw0po1nt Nighthawk
* Bobloblaw Zingo Labs
* Lux Zingo Labs
* Oscar Zingo Labs
* Daniel Wolande ZF
* John ZF