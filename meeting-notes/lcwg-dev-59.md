# Light Client Working Group Devs Meeting 59
### Meeting Date/Time: Thursday, Aug 31st, 2023 17:00 UTC
### Meeting Duration: 40 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: @nuttycom (ECC), Conrado (ZF), Adi (NH), Matt (NH)
### Notes: @pacu

## General Notes

### ZF Updates

Decentralistdan will be leading the ZIP-317 ecosystem outreach and asks insights from the 
rest of the attendees. Asked for some leads or recommendations to take on this process.

Kris suggested mentioning the 10000 zat minimum fee as a least effort pseudo-compliance with the
fee structure. For the case of miners, if they know the structure of their transaction beforehand, 
they could estimate a 5000 zat fee per action.

Also proposes that when moving this call to a bi-weekly cadence, using the intermediate week slot for FROST dev call. (This was agreed by all present people.)


### NH Updates 
Matt: more of the question than update, thanks Kris for merging a [PR](https://github.com/zcash/ZcashLightClientKit/pull/1210), and ask if the last commit hash of the iOS SDK will be pullable. 

Kris: they will be releasing a follow-up commit of a potential issue/edge case in the account birthday logic when there's a chain re-org that roll back funds prior to the wallet birthday. 

Matt: Is Secant codebase updated to last Sbs code?

Kris: He's pretty sure that the current versions are using the latest releases of the SDKs

### ZWCD Updates
Pacu wrapping up the first round of integration tests with darksidewalletd, which mean to
actually figure the precise data (TreeState, commitments, tree heights, etc.) the wallet
will need to sync the whole blockrange of the test. This is coupled to the sync algorithm
of choice.

Pacu asked ECC devs to, when possible, update the existing docs on DAGsync to reflect Sbs logic so that these tests can be also extended to cover the SDKs


### ECC Updates

Kris: 

- including account birthday in data access api. 
- providing new way of providing wallet balance, will have balance broken into: currently known, spendable, balance that will be spendable soon, change balance, unshielded balance.
- New notion of scan state, it will be reported in terms of note commitments that are left to scan since the last fully scan state. 
- appearance of sync state will be minimized and will prioritize synced balance. 
- sync progress will be moved into a detail screen and taken. 

#### SDKs pre-release testing 

The release candidates of the SDKs will be shared on the LCWG channel. 
