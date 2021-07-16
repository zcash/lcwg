# Light Client Working Group Devs Meeting 9
### Meeting Date/Time: Friday, July 16th, 2021 15:00 UTC
### Meeting Duration: 45 minutes
### [Agenda](https://github.com/zcash/lcwg/issues/15)
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
@pacu, @gmale, Wil Moore III,  Eljio Prifti, Adi(Nighthawk),  Mandeep Bhalothia, Piyush Sharma, Vamsi Krishna, 

## sync improvements

Kevin: update on sync enhancements throughout the ecosystem. ECC Wallet team is pairing up with Core engineers to discuss how to bring NU5/Halo to librustzcash and also discuss the possibility on improving syncing and bringing it on par with latest developments.

Adi: supports the strategy and comments that Vamsi is working on ivk import things

Vamsi: z_import_ivk on Zcashd and facing some performance problems. Zcashd takes around 8 hours whereas ZecWallet-lite takes one hour.

Kevin: Syncing improvemnts are in line with that feature. The SDKs already work with viewing keys. We should have this functionalities in mind when we do those improvements.

Vamsi is using the ZecPages viewing key to test which has a high number of shielded transactions

Kevin: we should focus on making scanning pretty low so that we can take it as an irrelevant thing and improve the user experience.

## Collect and submit feedback for ARTI

Kevin: This is delegated to Nathan and Steven from ECC.

Adi: there was a meeting about requirement on ARTI for Zebrad and mobile was brought up, although it will be prioritized around mid-next-year. A high level idea / requirement touch base call with the LCWG or part of getting proposals for bringing ARTI to mobile. 

Kevin: can we do the normal iOS/Android networking things without needed to bring a massive library, needing elevated priviledges, etc?

General: bring specific questions/concerns/requests to the table through a document to the ZOMG.


## iOS / Android 

Kudos to Nighthawk on responsible disclosure of the vulnerability found on iOS and how it was handled procedure-wise

Kevin: what could be put in place to improve the review process? ECC is evaluating software improvement process alternatives, one of them is bringing extra developers to specifically audit/review PRs

Eljo: Offered some hours of availability to that effort.

Pacu: we have a Request for Improvements/Suggestions for the next Wallet App development in terms of code structure, architecture, etc. 

Adi: Nighthawk can chime in with ideas on that front.

Kevin: Autoshieling in mobile is almost to a point we don't think it sucks

Adi: Nighthawk is adopting an automated translation service called lingo so he's going to work on android's string files so they work out with that service. Also offered an extra slot on his translation pack to make PRs to the android projects.

Pacu: once the autoshielding work is called done, we will address Nighthawk's request to add Biometric authentication to Backup Seed screen and fix other related bugs.

kevin: nice to have feature often get low priority in our queue, so calls to action to contributor that can tackle those. 



---------------------------------------

## Next Meeting
Light Client Working Group Devs Meeting #10, July 30th, 2021 @ 1500 UTC

[Next Meeting Agenda](https://github.com/zcash/lcwg/issues/TKTKTK)

