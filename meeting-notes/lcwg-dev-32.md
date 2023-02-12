# Light Client Working Group Devs Meeting 32
### Meeting Date/Time: Wednesday, July 27th, 2022 15:00 UTC
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
  - More work underway with Block height object type changes.
  - Discuss Wallet UX concerns - Scanning % progress is sometimes lost when restarting progress.
* Android
  - Next update will include block height api and smaller download batches
  - Unified address support will be a fast follow
  - Since NU5, increased the frequency of checkpoints, shorter interval between blocks improve wallet birthday
  - Further optimizations in downloading vs streaming block data
* iOS
  - Threading issue in iOS 16 debugging
  - Issues with large blocks - 
  - Increasing the timeout for lightwalletd connection to 30s from 10s, 100 s for streaming calls
  - Decreasing download batch size to 25 blocks or 10 blocks
  - Purge the cacheDB on app start as it grows fast purge back when syncing and on app restart
* Nighthawk
  - Updating SDKs
  - Unstoppable domains integration
  - Logging lightwalletd, to learn about service restart issues
  - Lightwalletd multiple registrars idea

# 2. Upcoming meeting related news
* August 10 LCWG meeting will not take place developers will meet in-person at Zcon3
* LCWG meeting time change to Thursdays at 14:00 UTC

## Attendees
* Adi @nighthawk24 Nighthawk
* @Pacu ECC
* @ccjernigan ECC