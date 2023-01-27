# Light Client Working Group Devs Meeting 42
### Meeting Date/Time: Thursday, January 26th, 2021 17:00 UTC
### Meeting Duration: 30 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Adi @nighthawk24, Carter @ccjernigan, Nick Takacs, Matthew Watt @tw0po1nt, Nathan Wilcox
### Notes: Adi

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| | ||


# 1. General Notes
* General
 - zcashd v5.4.0 release is upcoming
 - zcashd v5.5.0 and lightwalletd updates will follow with feature targets to support DAGSync related changes and ZIP-317
 - Vision - this group becomes a driver for protocol updates with more ecosystem participants using the Zcash SDK joining the call
 * Android SDK
  - ECC Wallet code merged
  - Newer SDKs v1.12 are incorporated
  - No known regressions
  - API 21 minimum supported level, target 5 years of android versions - trade offs on device history and security patches
  - Support for old reference wallets will be dropping soon
* iOS SDK
  - v0.18.0-beta is underway, ongoing work on tightening validating and scanning, delayed on a rust crate for file system related changes
  - May split the 0.18.0 beta release in to 2 till the rust crate is updated to include the missing libraries
  - In the next few weeks, a newer SDK will be released
  - ECC wallet has the changes included for the recently released SDKs
* Nighthawk feature request
  - Consider plans for reducing cofirmation count recommendation from 10 when making transactions
  - z_sendmany on Zcash SDKs (needs parser or use bridge from librustzcash, or serialize and deserialize)

## Attendees
* @Pacu ECC
* @ccjernigan ECC
* Nick Takacs ECC
* Nation Wilcox ECC
* @nighthawk24 Nighthawk
* @tw0po1nt Nighthawk