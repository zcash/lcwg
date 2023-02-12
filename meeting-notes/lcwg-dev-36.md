# Light Client Working Group Devs Meeting 36
### Meeting Date/Time: Thursday, October 20th, 2022 17:00 UTC
### Meeting Duration: 30 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Adi @nighthawk24, Carter @ccjernigan
### Notes: Adi

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| | ||


# 1. General Notes
* General
  - Major changes in Room lib removal PR
  - Introduce the new batch scanning changes, no noticeable syncing improvement
  - Change from exposing the room APIs to public, now it’s new type safe changes
  - Utilize simple types, no plan to modify the db unintentionally
  - Support for Unified Addresses, get address API changes, sapling is now legacy sapling address
  - No plan on supporting multiple accounts, instead supporting account index 0 to n
* Android SDK
  - Android 0 simply the initialization, instead pass params in synchronizer to create a new object
* iOS SDK
  - iOS improvements on concurrency
  - Basic changes to go out in the next release, advanced ones to follow

## Attendees
* @nighthawk24 Nighthawk
* @Pacu ECC
* @ccjernigan ECC