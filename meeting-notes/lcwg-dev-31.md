# Light Client Working Group Devs Meeting 31
### Meeting Date/Time: Wednesday, July 13th, 2022 15:00 UTC
### Meeting Duration: 45 minutes
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
  - Discuss block syncing issues surrounding lightwalletd
* Android SDK
  - ECC updated reference wallet to use Android SDK v1.7.0
  - Android v1.8.0 will be a larger change - refactoring around wallet birthday and initialization is expected
  - Android SDK update will move all database files to a no-backup directory to increase privacy & security of user's transaction history
  - Android SDK's future plan is for getting atomic wallet birthday on wallet creation
* iOS SDK
  - iOS working on 0.16 ZcashLightClientKit - non-breaking changes
  - Plan on deprecating APIs instead of removing them, this makdes it easier to transition for apps that use ECC Mobile SDKs
  - Plan to document the server errors into readable messages for end users
  - Work in progress towards adding localization
  - Fresh checkpoints are being generated for new releases of ZcashightClientKit
* Nighthawk Updates
  - Removed hardcoded checkpoints
  - Made new releases with updated SDKs for both iOS and Android
  
## Attendees
* Adi @nighthawk24 Nighthawk
* @Pacu ECC
* @ccjernigan ECC