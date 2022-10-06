# Light Client Working Group Devs Meeting 33
### Meeting Date/Time: Wednesday, August 26th, 2021 16:00 UTC
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
  - Several new releases with refactoring, moved DB to no-backup option
  - Latest SDK release is stable
  - Upcoming: Changes towards DB performance improvements, ORM calls are out of public APIs, improvements to fix Sapling scanning
  - synchronizer.restart function is gone - need to manually close and make a new one if required.
* iOS SDK
  - SDK 0.16.7 fixes on queue priority
  - Updated checkpoints
  - Use block streamer to improve the download stage
  - Adopt new concurrency changes
* Nighthawk Updates
  - Shipped updated SDK to users

## Attendees
* Adi @nighthawk24 Nighthawk
* @Pacu ECC
* @ccjernigan ECC