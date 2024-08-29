# Light Client Working Group Devs Meeting 82
### Meeting Date/Time: Thursday, August 8th, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Kris (ECC), Andrew (ezcash), Conrado (ZF), Pili (ZF), Za (Zingo), Fluid vanadium (Zingo), Za (Zingo)

## Agenda:
- Quick team updates 

ZIP-320 integrated in librustzcash. But it requires additional changes on how transparent wallet history is handled because of how UTXOs are handled to implement autoshielding in the SDKs which is incompatible with how they should be handled to restore transparent transaction history. This entails updating ligthwalletd RPCs to walk the chain forward. (see requirements). See call to action for getrawtransaction issues.


- Decentralizing Core development: 
  - Lightwalletd and Zebrad RPC issues affecting wallets: fixes and deployment plans
  - Implementing Zingo Indexer.
- Roadmap to mobile Hardware wallets:
  - Brainstorm Requirements 
  - Partial Zcash transaction format
  - Changes to transaction builders
  - general purpose SDKs 
- Orchard API and ZIP-312 implications for FROST’d wallets
  - https://zips.z.cash/zip-0312’
  - https://github.com/pacu/frost-uniffi-sdk/pull/65


## decentralizing Core development
Someone needs to fix this https://github.com/zcash/lightwalletd/issues/493
ZF Zebrad team is adding this to the NU6 backlog https://github.com/ZcashFoundation/zebra/issues/8744
Zcashd wallet deprecation: Forward walk of the blockchain complete transparent Zcash support 
Fluid Vanadium: What’s the standardized set of RPCs for lightclients that the zingo indexer needs to implement? According to Kris, the service.proto is the standard set of RPCs at the moment.
What’s needed to implement Zingo Indexer as a rust implementation more feature-rich replacement of lightwalletd?
Za: from a 30,000ft PoV i’m not sure what the set of requirements should be
Kris: there are two indexing components: one for Block Explorers and one for offloading scanning viewing keys to a service.
Link to the diagrams of the scanner: https://github.com/zcash/librustzcash/issues/1373#issuecomment-2076019340 
Pacu: how can we gather all these requirements in one place to work them out?


 
## Roadmap to Hardware wallets
We couldn’t discuss this because of lack of time.
## Orchard API and ZIP-312 implications for FROST’d wallets
	- The missing bits of the ZIP is how to generate a FROST wallet, there are many ways to do it and it has to be discussed what is the best approach agree on it and put in in the ZIP. 
Transaction plan format  and randomizer handling
Has FROST been appointed as official threshold sig for NDFM? 
No it hasn’t there are questions around signature attribution and robustness of the protocol
According to Conrado attribution can be worked out by publishing verifying shares.




Zebrad indexer requirements:
ZI1: Index to walk the blockchain forward (through outpoints) 

Zingo indexer requirements:
Required information to implement ZI1.
Make sure that the bugs specified in the issues linked below are not reproduced by it


## Calls to action

- Getrawtransaction issues 
- https://github.com/zcash/lightwalletd/issues/493
- https://github.com/ZcashFoundation/zebra/issues/8744

