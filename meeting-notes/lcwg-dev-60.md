# Light Client Working Group Devs Meeting 60
### Meeting Date/Time: Thursday, Sep 7th, 2023 17:00 UTC
### Meeting Duration: 40 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: @nuttycom (ECC) @str4d (ECC), Adi (NH), Matt (NH) Mandeep (NH), Dan Forbes (Chainsafe)
### Notes: @pacu

## General Notes

Agenda:
- LCWG Repo notes not being merged. We should host this repo elsewhere. 
- Calendar Setting of Zoom call
- Team updates

### Meta
#### LCWG Repo
Kris will merge the outstanding PRs and Pacu and Decentralistdan will be added as
contributors

#### Calendar setup
Decentralistdan will figure how to setup a Zoom Seminar calendar for this meeting, 
and also schedule it Bi-weekly as Arborist is. This call will alternate with 
a FROST Dev call that take the place of the old "Zeal Calls" the idea is that 
all LCWG attendees are invited to the FROST dev calls to contribute to that 
development with requirements, feedback, etc. 

### ECC Update

Kris: on track with wallet SDK Sbs release candidate tomorrow (Friday 8th).
Doing final testing. Branch: `feature/DAG-Sync`

Str4d: Zcash FFI framework on iOS is broken on `main` due to miscommunication
causing a PR being merged incorrectly. However, at this point `feature/DAG-sync` has all of the relevant changes and should be where all future changes prior to the SDK release appear.

Equivalent PRs for Android are on https://github.com/zcash/zcash-android-wallet-sdk/tree/fast-spendability



### NH Updates

Mandeep: working on Fiat conversion feature on NH's app for Android

Matt: waiting for SDK updates and working on NH's app feature.

### ZWCD Updates
- SFoE and first milestones are completed. Str4d has 200k block datasets for zcashd
  that might be useful for wallet testing. These datasets will produce wallets with 200k notes
  received and 200k note spends to sync. There's a blocking element which is that they are not
  HD Seed accounts so there might be some work to be done to actually use them 
- Reported Regtest issues on Zcashd repo to document issues either for fixing or
  for Zebra development of Regtest feature.
- Idea of creating newer AdvancedReOrgTests datasets on Regtest which will require
SDKs to support Regtest (Feature request open as well)
- Pacu will be Out of Office from 14th to 28th of September. Dan or Adi could fill
  in for him in note taking.


### Chainsafe Updates
During the second half of the meeting Dan from Chainsafe joined.
His team is looking to create a Javascript SDK for Zcash. 
They are creating a Draft document to present to the Community which he shared 
privately with attendants.

Regarding some comments @pacu had made on that document about ZIP-321, they are 
considering that as a follow up feature for proposal.

Str4d: adviced using the zcash rust backend crate and take it from there

Dan: is it possible to send funds without a fully synced walled?

Str4d and Kris pointed Dan's team to relevant documentation of their current 
developments on that matter. There are also limitations with the WASM enviroment 
like the threading model and database access that need to be worked around. 

Dan feels that the project research is going in a positive direction and they
are thrilled about the possible outcomes. 

Decentralistdan will share the document Draft with ZCG on their Friday brainstorming
Session tomorrow 

