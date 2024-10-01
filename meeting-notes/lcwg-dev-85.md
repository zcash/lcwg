# Light Client Working Group Devs Meeting 85
### Meeting Date/Time: Thursday, September 19th, 2024 17:00 UTC
### Meeting Duration: 50 minutes
### Moderators: @decentralistdan - ECC, Pacu (ZecDevRel)
### Attendees: Wollum and Eric (chainsafe), Conrado (ZF), Zancas (Zingo), Str4d (ECC), Jason (ZCG)

### Agenda

- Team updates
- iOS 18 updates! Heads up!!
- If chainsafe is present, In-Memory Wallet status (https://github.com/zcash/librustzcash/issues/1414) 
- ZIP 320 statuses towards Sept 20th.
  - Zingo
  - ECC SDK client wallets (Nighthawk, Unstoppable, Edge)
- Status of Partial transaction format for Hardware wallets and FROST

# Team Updates

**Zingo:**
- librustzcash and Zingo’s fork diverged to they are completing the convergence. They expect to have it by the

**ChainSafe:**
migrated test to sqlite crate to the zcash client back end to be used with any backend. 
In Memory wallet passes their full test suite. 
All of the above works in the wallet.
Benchmarks with ZecPages seems reasonable. 
Think they’ll be able to ship on time. 
There’s a demo wallet front end to dogfood the Web JS sdk
A blocker is that Zcash transaction creation separation to be able to not store keys in the web app. Mid-October this will become a full blocker to complete the snap 

Status of Partial transaction format (PCZT) for Hardware wallets and FROST:
- There’s transaction construction steps
- There’s a proof building step
- Then the authorization of the PCZT is done
- The proved PCZT and the authorized PCZT are merged and the transaction is created. 

No progress has been made. Input is being gathered to know how the different wallets will be using PCZT. https://github.com/zcash/zips/issues/693

Chainsafe will share their list of requirements  

Str4d will try to resume the refactoring to achieve this but he was blocked by ZIP-320 work 

### ZIP-320 Retrospective, when is it a good time to do it?
Str4d: If so there should be 2 different retrospectives one for the engineering side and one for the outreach we wouldn’t want to mix those two.
