# Light Client Working Group Devs Meeting 30
### Meeting Date/Time: Wednesday, June 29th, 2021 15:00 UTC
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
  - Carter intro
  - New Moile SDKs in the works: v1.6.0 on Android & 0.16 on iOS
  - Currently the Client App resources are setting custom checkpoints - SDK can take care of auto checkpoint updates on version releases
  - DAGs updated for ECC wallets https://zcash.github.io/developers
  - iOS Synchronizer pending issue:  when users are backgrounding the app and they resume - GRPC channel dying and not resuming as expected and then the app errors out
  - Android crashes when networking errors out when the app in the background
  - GRPC team is in touch with ECC devs for advice on how to use the APIs for native apps
  - Bumping up minimum Android API to iOS 13, to have a coroutines equivalent on iOS
  - iOS ZcashLightClientKit 0.16 will include changes on the Birthday API
  - Additional changes on cleaning up the Oublic API for being more type-safe usages around Zatoshi object & memo encoding.
  - Upcoming large effort - changes with Unified Address will be major, possibly breaking.
  
## Attendees
* Adi @nighthawk24 Nighthawk
* @Pacu ECC
* @ccjernigan ECC