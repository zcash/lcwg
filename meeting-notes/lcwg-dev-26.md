# Light Client Working Group Devs Meeting 26
### Meeting Date/Time: Wednesday, May 4th, 2021 15:00 UTC
### Meeting Duration: 45 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Adi @nighthawk24, Dmytrii
### Notes: Adi

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| | ||


# 1. General Notes
* Nighthawk Updates
  - Share progress & walkthrough UI for Wallet, Transfer Send/Receive flows and Settings screens.
  - Discuss lowering confirmation count, WIP with the goal to improve UX for auto shielding & migrating and fast confirmations configurable with the wallet.
  - Discuss adding a send to many API in SDK using Payment Request.
* General
  - Android Pre Halo Bugfix release coming soon.
  - iOS switch to using swift package manager to support the checkpoints to be separately set.
  - SDK with swift package manager on ECC wallet saw build time improvements
  - Issues around swift package manager affects any library as it ends up affecting all projects with Xcode. Hence the support for faster builds and XC framework format for apple system to bundle every arch Intel, ARM and the platform automatically bundles required dependencies.
  - Upcoming releases that will be testnet ready: Android SDK 1.4.0 Beta & iOS ZcashLightClientKit 0.14.0 Beta.
  - Discuss ideas around auto bundling checkpoint during build process vs manually adding verified checkpoints when shipping releases to users.
  
## Attendees
* Adi @nighthawk24 Nighthawk
* Dmytrii Nighthawk
* @Pacu ECC