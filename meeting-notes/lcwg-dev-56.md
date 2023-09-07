# Light Client Working Group Devs Meeting 56
### Meeting Date/Time: Thursday, Aug 10th, 2023 17:00 UTC
### Meeting Duration: 30 minutes
### Moderator: @pacu - ZWCD
### Attendees: @nuttycom (ECC), John (ZF), Matthew Watt (NH), Mandeep Bhalothia (NH)
### Notes: @pacu

### 1. General Notes
#### ECC SDKs:
**Fast spendability (Spend Before Sync):**
- There is API stability on the SDK branches for developers to use the github branches to code against, and they are being improved in terms of bugs and other hiccups.
- public pre-release tags and versions will probably be out next week (Aug 14-18)

**ZIP-317 Fees:**
- There is an issue where the fee field is zero instead of the actual fee when retrieving the transaction
- The implementation will have a "proposed transfer" returned from the "createToAddress" API, that will contain a protobuf with several fields like: zip-321 payment URI representing the proposed transaction, the balance of the transaction, the privacy implications for the wallet to execute it.
- once the above is finished the ZIP-317 fees will be "turned on" on wallets. 
- ideally there will be an additional API to a ZIP-321 payment request as input for generating an transaction proposal protobuf for then the user to validate and submit.

**Darksidewalletd** 
- There are some other work pending for fast spendability to be supported on darksidewalletd.

#### Meta: LCWG 
- LCWG handover to from ECC to ZWCD is still pending
