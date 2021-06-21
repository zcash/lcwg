# Light Client Working Group Devs Meeting 6
### Meeting Date/Time: Friday, May 28th, 2021 15:00 UTC
### Meeting Duration: 1 hour
### [Agenda](https://github.com/zcash/lcwg/issues/7)
### [Video of the meeting](not-recorded)
### Moderator: Kevin Gorham
### Notes: Adi

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| **Action 1** | Larry: can I ask Lightwalletd about a specific hash? (tx id??)||
| **Action 2** | Pacu: send invite to add adi to testflight||
| **Action 3** | Kevin: PR review for swapping out Lockbox Mandeep ||
| **Action 4** | Kevin: PR review for Adi||
| **Action 5** | Kevin: Identify next feature for Elio||
| **Action 6** | Research: signal’s open APIs for authentication and secure private||

# 1. General Notes
- Kevin: presented next term strategy for wallet and SDK development from ECC. We will add Adi to ECCs testing builds
- Right now, we don’t have auto-shielding enabled
  - So if a user hasn’t checked on their balance, it might actually be transparent at rest
- We want to move from “pool minded” to “balance minded” funds
- Since you own both addresses, we might be able to do auto-shielding with fewer confirmations
- https://github.com/groue/GRDB.swift/blob/master/Documentation/WhyAdoptGRDB.md#core-principles 
- Potentially register .z2z with handshake devs
  - https://en.wikipedia.org/wiki/Open_Whisper_Systems

-------------------------------------------
## Attendees
- Kevin
- Pacu
- Adi
- Geffen
- Elio
- Mandeep 

---------------------------------------

## Next Meeting
Light Client Working Group Devs Meeting #7, June 11st, 2021 @ 1500 UTC

[Next Meeting Agenda](https://github.com/zcash/lcwg/issues/8)

