# Light Client Working Group Devs Meeting 81
### Meeting Date/Time: Thursday, July 25th, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Pili (ZF), John (ZF), Conrado (ZF), Andrea (ECC), Kris (ECC), Zancas (Zingo), Jason (ZCG) 


## Agenda:
- Quick team updates 
- ZIP-320:  deployment of TEX addresses (almost there!)
- Decentralizing Core development
- Brainstorm Ideas for a new initiative!

### ZIP-320:  deployment of TEX addresses
ZIP-320 work has been merged and is being tested at the moment. There are some bugs being worked on at the moment. There is not an alpha version  yet to share with partners like EDGE, Unstoppable or Nighthawk.

There’s a problem with TEX address transactions when restoring wallets. Not strictly related to 320 support but still a side-effect from it. 

According to what Kris estimates, they  could be cutting an alpha release soon.

### Zebrad regtest, ZingoProxy and Darksidewalletd work

It was mentioned in today’s arborist call that there was substantial work on implementing Regtest support on Zebrad and many RPCs on zingo proxy mostly focused on NYM support but with extra work could be extended to replace current GoLang implementation. 

This is relevant to bringing back to life darksidewalletd tests for non-linear sync. There’s another piece of work from ECC in the zcash_client_backend crate that allows developer to create a fake chain with the corresponding shardtree data to make syncing coherent with the test data. Although this is coupled with shardtree and there would have to be work to generalize it.

### ZIP-315 best wallet practices and ZIP-316 compliance
Zashi and other SDK wallets use internal addresses for change and other wallets don't, so there's a mismatch on available balance when it comes to loading the same keys on different addresses. Zingo is using the external address to send change. 
If Zingo gets zcash_keys crate in then they will be able to fix this internal address. Their main blocker is a severe bug inherited from ZecWallet where BIP-44 derivation is implemented wrong and their existing users have problems when generating new addresses or restoring wallets. Zingo will have to accommodate both new and existing users, having backwards compatibility with the buggy code in order for their affected users not to lose funds.  This is being a major pain for them since it block them to further advancing their integration with librustzcash crates. 

### FROST integration with Zingo
According to Zancas, Zingo’s priorities are ZIP-320, NYM, hardware wallets support and lastly FROST. Although, there is some work overlap between HW wallet support and FROST given the need to decouple transaction signatures from the transaction builder. This is also something that Pacu and Conrado are currently working on (separately but they should get together to avoid repeated work).

Kris brought up the PR [1388](https://github.com/zcash/librustzcash/pull/1388) on librustzcash that is starting that work. Unfortunately what’s needed to be done is quite subtle and would be hard for others to take on. Pacu suggested that the PR is worked on so that others can actually help out and contribute with Str4d instead of just wait for him to have cycles to finish that work. 

Work on the Orchard crate is progressing in terms of finding a suitable approach so that FROST requirements are not available to those who will inadvertently use those APIs and then end up with key material that is impossible to use for key restore. This was suggested proactively by Pacu and agreed with Daira-Emma Hopwood over Z | ECC. 