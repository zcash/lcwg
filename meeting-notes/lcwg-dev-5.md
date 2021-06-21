# Light Client Working Group Devs Meeting 5
### Meeting Date/Time: Friday, May 21th, 2021 15:00 UTC
### Meeting Duration: 1 hour
### [Agenda](https://github.com/zcash/lcwg/issues/6)
### [Video of the meeting](not-recorded)
### Moderator: Kevin Gorham
### Notes: Adi

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| **Action 1**   | Eljo needs more work assigned to him | [33:51](no-video) |   
| **Action 2**   | Piyush and Pacu to carve out some 1on1 time to solve dev environment issues | [53:42](no-video) |    

# 1. General Notes
- Kevin: we are planning to start NU5 + App changes to ECC wallet that is not a full revamp but is close to that. We want to coordinate with Nighthawk to discuss the impact of those changes. ECC’s objective is to focus on the SDK as its product, and the wallet is just software that tests and experiments with SDK features on people’s hands. There’s been conversations about creating a separate repo for the new version of the ECC wallet. 
- Adi: NightHawk is considering ECC’s current theme as their Dark theme and Matt is working on a different theme on their redesign efforts. 
- Brad: we are aiming to reduce complexity on the Wallet Application to adjust to the size of our team to be able to focus more on new features that the SDK provides and less on wallet maintenance. We don’t want to disrupt NightHawk’s work so we are not ruling out creating a separate repository for the new phase of the ECC Wallet. 
- Adi: doesn’t think that it would be problematic to adopt whatever UI that comes out for that effort because they don’t want to add any work to their queue at least for this year. Brought up sync times and users inconvenience
- Pacu: We need to improve background task handling on both fronts. Callout to contributors that have knowledge and experience on that.
- Adi: Brings up new Android 12 backwards compatible features
- Pacu: For upcoming week, there will be a tech debt work ½ week. iOS will try to tackle syncing refactoring and Android will focus on removing Channels in favor of Mutable State Flows 
- Vamsi: Lightwalletd from lightwalletd.com will upgrade to 0.4.7 
- Brad: Price Oracle will be added on PR from Zec Wallet Developer Aditya Kulkarni. 

-------------------------------------------
## Attendees
- Kevin
- Pacu
- Adi
- Brad
- Wil
- Elio
- Matt
- Mandeep
- Vamsi 

---------------------------------------

## Next Meeting
Light Client Working Group Devs Meeting #5, May 21st, 2021 @ 1500 UTC

[Next Meeting Agenda](https://github.com/zcash/lcwg/issues/6)

