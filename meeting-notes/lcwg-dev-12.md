# Light Client Working Group Devs Meeting 12
### Meeting Date/Time: Friday, August 27th, 2021 15:00 UTC
### Meeting Duration: 45 minutes
### [Agenda](https://github.com/zcash/lcwg/issues/21)
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Notes: Pacu Gindre @pacu

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| | ||

# 1. General Notes
-------------------------------------------
* ECC Updates
 - New contributor onboarding.
 - NU5 updates. Status of Audits. Release candidate for Zcashd planned for incoming week
 - Work will be mainly focused on NU5 preparations on the SDK front and the new wallets
 - ECC Reference wallets will enter "maintenance mode".
 - SDKs will aim to include some flavor fast sync algorithm
 - Studying FFI approaches to support advanced integration between native and Rust layers.
 - 
* Nighthawk updates
 - Reviewing and maintaining Google Play and App Store crashes. 
 - Adding Zcash URI Support for QR codes
 - Wallet Sweeping functionality to allow paper wallet handouts. 
  - Pacu suggested checking out liberated payments docs: https://github.com/zcash/zips/pull/420/files
  - Pacu's suggestions: Wallet Eject Button to move funds in case of emergency (keys tampered, privacy leak, security issue, etc)



- Android updates:
  - Will Secant wallet use the same key storage scheme? 
   - We really don't know. probably SecOps will advice adopting the latest and greatest available.
  - Will the new wallet be installed on top of the old one? 
   - no, they are separate wallets
  - Will they be open source from day 1?
   - yes, they are already open sourced on our github repo.

## Attendees
* Steven, and @pacu
* Adi and Mandeep from NightHawk

## Next Meeting
Light Client Working Group Devs Meeting #Friday, September 10th, 2021 @ 1500 UTC

[Next Meeting Agenda](https://github.com/zcash/lcwg/issues/TKTKTK)

