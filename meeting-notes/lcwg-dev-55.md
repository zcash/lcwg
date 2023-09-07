# Light Client Working Group Devs Meeting 55
### Meeting Date/Time: Thursday, Aug 3rd, 2023 17:00 UTC
### Meeting Duration: 15 minutes
### Moderator: @pacu - ZWCD
### Attendees: @nick-ecc (ECC), @nuttycom (ECC)
### Notes: @pacu

### 1. General Notes
#### ECC SDKs:
- Fast spendability: 
    - Android just had a release on maven central and will possibly have another following up within the next few days.
    - There's a caveat where Developers should pause syncing when users attempt to start the send flow on their wallets to avoid `database locked` errors.
#### Request for Help to ZWCD:
- There are Wallet related PRs on librustzcash that would be helpful to have extra reviews on:
    - [Restrict use of backend-specific note identifiers](https://github.com/zcash/librustzcash/pull/888) 
    - [Fix a number of bugs related to the creation of change memos and storage of empty memos](https://github.com/zcash/librustzcash/pull/886)

#### Meta: LCWG 
- Nick and Pacu will meet next week (Aug 7-11) to define which things need to be handed over to ZWCD.


