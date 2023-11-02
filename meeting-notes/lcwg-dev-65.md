# Light Client Working Group Devs Meeting 65
### Meeting Date/Time: Thursday, Nov 16th, 2023 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Kris (ECC), Zooko(ECC), James Mudgett (Brave), John (ZF), Hazel (Zingo), Pili (ZF)

## Agenda:

### Presentation Slot: (optional)
    - this is a previously requested slot by any developer wanting to present
    - This Slot is taken to discuss Meta topics by Dan and Pacu
    
### Meta:
  - LCWG schedule: Is this time convenient for most participants?
  - LCWG Repo: where should it be hosted? 
  - Would it be helpful if this call was recorded as Arborist calls are? Would you be ok with it? (not discussed)

### Team Updates: 2-3 minute updates per team. Shorter is better
  - Kinds of team updates:
    - General Status 
    - Request for input
    - Announcements
    - Blockers or dependencies with other teams

### Workgroup’s initiatives
  - Here we will establish what are the group's initiatives that we'd like to focus on.
  - some off-the-cuff initiatives:
     - Develop and maintain Light Client infra 
     - ZIP-317 support beyond minimum fee 
     - ZIP-315

    
## General Notes

### DST and LCWG
We had some issues regarding scheduling and DST changes that have been figured and the calendar events will be fixed.

### Meta:
Pacu explained the new call structure and the goals of the “all new” LCWG. 

Decentralistdan and Kris sorted out the DST scheduling chaos and defined the time for the calendar invite that will be modified. 

### Team Updates

#### ECC
**Priorities**: Orchard support on Librustzcash crates  backend and sqlite
As a third-tier priority, below Orchard and ZIP 317, we have in flight some additional improvements to the Spend-Before-Sync algorithm intended to make the user experience fewer delays when they open their wallet.

**Request for input**: https://github.com/Electric-Coin-Company/zcash-light-client-ffi/pull/105 PR created TwoPoint from NightHawk

**Request for input**: ECC is working on a concept of “spendable balance” that works along with ZIP-317. They will be testing their PoC on Zashi with beta testers and then send a draft proposal to LCWG to discuss widely.

#### Zingo
**Priorities**: 
- shardtree upgrade to incremental witness trees
  - work on squashing some bugs before release. 
  - Address book and Address authentication

#### Brave
James introduced himself, and walked the group through their Brave Wallet sending Zcash t2t 

### Team Initiatives

Three possible initiatives were discussed:
- ZIP-315 support of best practices for Zcash wallet
- Implementation of ZIP-317 across the ecosystem
- Lightwalletd maintenance and support ZIP-307 / Decentralize Core development

Workgroup initiatives are meant to be more than declarative and produce actual results and deliverables. We aim to achieve some level of cross-team commitment in terms of work allocation of all kinds, from management, steering, development, review, etc.

#### ZIP-315 support of best practices for Zcash wallet
This initiative means to iterate and finish the draft of this ZIP and subsequently implement across the different wallets. Currently wallets aren’t managing funds consistently in the way that they can’t be interchangeably used. Putting the seed phrase recovery and reuse issue, crypto users expect their balance holds across different wallets which is not the case for Zcash wallets.

#### Implementation of ZIP-317 across the ecosystem
Wallets must support ZIP-317 fees beyond the minimum fee of 10000 zats. There are development and UX aspects to cover that need to be worked on when passing from the concepts of the ZIP to the reality of wallet applications.

#### Lightwalletd maintenance and support ZIP-307 / Decentralize Core development

Although lightwalletd source code is hosted by ECC, this is a legacy disposition. Currently ECC has expressed concerns on their ability to keep supporting maintenance of ZIP-307 implementation in GoLang known as Lightwalletd.  Pacu expressed this is an urgent matter since we don’t currently have active owners that can review any PRs needed to support enhancements that LWD needs to support new Zcash features such as DAG Sync or Spend before sync, or its darkside testing counterparts. 

Zooko proposed a “decentralize core” initiative that mimics the decentralization effort for Zcash Digital

### Presentation Slot (Ad hoc)
We even had a great spontaneous demo of Brave Wallet using Zcash! 


### Actions Items for previous call
- Bring up Lightwalletd codebase maintenance and support as an ecosystem issue
  - this has been included as one of the workgroup initiatives.
