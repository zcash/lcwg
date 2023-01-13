# Light Client Working Group Devs Meeting 39
### Meeting Date/Time: Thursday, December 1st, 2021 17:00 UTC
### Meeting Duration: 30 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Adi @nighthawk24, Carter @ccjernigan, Kris @nuttycom, Gygaxis, Bobloblaw, Jack Gavigan, Daniel Wolande
### Notes: Adi

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| | ||


# 1. General Notes
* General

 - Zingo Labs developers shared the issues around Transaction Builder and Kris responded
 - Issues around clarity of creating a PR and what the process is, and timeline of feedback.
 - Identify ways for community members to help with PR triage, reviews and contributions.
 - Review policy currently is x number of PRs for y type of code for z type of developer. 

https://github.com/zcash/secant-android-wallet/blob/main/.github/pull_request_template.md
https://github.com/zcash/secant-android-wallet/tree/main/.github/ISSUE_TEMPLATE

 - ZIP 317 support is now available from librustzcash, and has at least been made available to the IOS SDK (I believe the Android side is in progress.) but not enabled due to lack of testing. Zcashd support is blocked on the completion of https://github.com/zcash/zcash/pull/6217
 - It isn't enabled yet on mobile, because we have UX concerns that aren't addressed yet. specifically we need to help clients convey estimated fees to users. The code to turn it on is present, but it is toggled off and not exposed in the public API.
 - Transaction proposal state - inputs are selected and outputs are assigned, fees are combined. Fixed point to reach where you add an input and there isn’t enough balance for fees.
 - Mobile SDK function does both computation plus signing at once. Ideally, the fees for the tx. should be shown the user at the transaction confirmation time. Background DAGSync may need to be paused when the user is in the Send transaction flow to handle concurrency issues.

* Android SDK
  - Performance  benchmarks, new SDK in next week
  - PR targeting the snapshot release.
  - https://github.com/zcash/zcash-android-wallet/pull/348
* iOS SDK
  - 0.17.0 is released.
  - 0.17.1 in progress with state handling and performance change on the wallet UI. Aim to shorten the cycle of scanning large blocks.
  - No API breaking changes.

## Attendees
* Adi @nighthawk24 Nighthawk
* @Pacu ECC
* @ccjernigan ECC
* Kris @nuttycom
* Gygaxin Zingo Labs
* Bobloblaw Zingo Labs
* Jack Gavigan ZF
* Daniel Wolande ZF