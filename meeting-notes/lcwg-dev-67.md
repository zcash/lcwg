# Light Client Working Group Devs Meeting 678
### Meeting Date/Time: Thursday, December 14th, 2023 17:00 UTC
### Meeting Duration: 40 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: : Za (Zingo), Kris (ECC), John (ZF), Pili (ZF), Conrado (ZF)

## Agenda:
- Team quick updates 
  - Workgroup Initiatives
  - ZIP-315 finalization and support across the wallet ecosystem: 
     - Pacu will be facilitating and coordinating work for this initiative. We will discuss the first items to work on async. 
     - Teams should: appoint team members that will participate and contribute to this initiative
  - Implementation of ZIP-317 across the ecosystem:
    - Dan will be steering this initiative (with some support of Pacu if needed)
    - Teams should: prepare to state their ZIP-317 compliance status and roadmap so we can start working on actions to work on. Additionally if needed commit resources to this initiative.
  - Lightwalletd maintenance and support ZIP-307 / Decentralize Core development
    - Lead/facilitator for this is actually vacant. There was an idea of imitating what was done on “decentralizing digital”. Group should decide on it and figure out immediate/short term steps to do it if so. 
- Pending Action Items from last LCWG

### Presentation Slot: (optional)
None requested.

### Team Updates: 2-3 minute updates per team. Shorter is better
  - Kinds of team updates:
    - General Status 
    - Request for input
    - Announcements
    - Blockers or dependencies with other teams

#### Pacu (ZWCD): 
work on ZIP-321 for Swift and Kotlin, reviewing ZIP-315 PR to start work on the initiatives.

#### Kris (ECC): 
working mostly on orchard support on librustzcash. There’s some input for ZIP-315 in terms of padding policies for transactions, what the padding policies are and when they should be applied. Also breaking out sapling crypto crate.

**Request for input/Collaboration:** Sean Bowe started a Zcash transparent script interpreter and constructor in Rust. It be nice to have Rust library that implement transparent.

#### ZF (Pili and Conrado):
Working on FROST, trying to figure out how to make wallets interact with each other to distribute signatures

#### Zingo (Za)
- Working on new release, networking issues and other enhancements like shardtree.
- Interested in working with Zebrad and deprecating use of Zcashd and lightwalletd.

#### Dan (ZF):
- IBC, what shall we do as light client working group?
- Asked Pili and Conrado about Lightwalletd integration w/ Zebra and what’s its status and work needed.


### Workgroup’s initiatives

Three possible initiatives were discussed:
- ZIP-315 support of best practices for Zcash wallets
   - Needs lead to arrange meetings and zip editing. Pacu will volunteer if no one else does (not out of laziness but to open up the game to others)
- Implementation of ZIP-317 across the ecosystem
  - Decentralisdan could have some bandwidth 
- Lightwalletd maintenance and support ZIP-307 / Decentralize Core development


#### ZIP-315:
- Pacu will be appointed for leading the initiative. He started reviewing the ZIP (again) and identifying pieces or work that can be assigned to others volunteering for this initiative. This work wasn't accounted for so it's being done on a low priority. 


#### ZIP-317:
- Dan will start putting together a comprehensive list of wallets and do a contact list, check what’s their level of implementation.

#### Decentralizing Core Dev: 
- Zancas will be appointed to lead the initiative, organize the work and coordinate with contributors.

Possible things to be done:
- Decide what to do about Lightwalletd and darksidewalletd and how to plug/integrate them to Zebra
- Regtest mode, how to sunset Zcashd support without losing that development and testing tool?
- Rust Implementation of Lightwalletd and darksidewalletd?


### Actions Items for **Next** call
- [DONE] ~~Need to define Leaders for initiatives and teams to define some minimum degree of
commitment to dedicate some hours to work in the initiatives.~~
