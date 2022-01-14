# Light Client Working Group Devs Meeting 10
### Meeting Date/Time: Friday, July 30th, 2021 15:00 UTC
### Meeting Duration: 55 minutes
### [Agenda](https://github.com/zcash/lcwg/issues/17)
### [Video of the meeting](not-recorded)
### Moderator: Kevin Gorham @gmale
### Notes: Pacu Gindre @pacu

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| | ||

# 1. General Notes
-------------------------------------------
## Attendees
- @pacu
- @gmale
- Eljo
- Adi (Nighthawk)
- Mandeep 
---------------------------------------

- General:
  - Questions
  - PRs
  - SDK release
  - Upcoming changes


- iOS:
  - nothing in particular 

- Android:
1. Nighthawk lightwalletd disconnection issue.
2. Lockbox migration.
3. USD price fetching via lightwalletd.

## Notes
- Less about missing features and more about community misalignment
  - Cannot afford this because we are a really small community
  - We should try to push forward and bring people in
  - Imagine being able to switch sync strategy
- Changes in Android:
  - Off by one (ten) error on autoshielding.
- Changes on iOS:
  - Network Agnostic implementation
  - Off by one (ten) error on autoshielding

## Action Items
- Make github issues around PendingTransaction DB
- Should unstoppable work for diversified addresses
- Fast sync update
- Try connecting the ECC wallet to the Nighthawk wallet
- Larry : review USD price endpoint
  - Necessary for FDroid
  - This app does not have any anti-features
- Create backlog tickets for mempool
  - Could be a good use-case for notifications
  - Look into scalability of mempool feature
  - Could lead to breaking all light clients and crashing price
- Kevin: Comment on the PR around lockbox
- Kevin: Look at navigation, particularly around back button on the landing fragment


## Next Meeting
Light Client Working Group Devs Meeting #11, August 13th, 2021 @ 1500 UTC

[Next Meeting Agenda](https://github.com/zcash/lcwg/issues/TKTKTK)

