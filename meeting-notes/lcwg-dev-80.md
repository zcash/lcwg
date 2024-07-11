# Light Client Working Group Devs Meeting 80
### Meeting Date/Time: Thursday, June 27th, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Conrado (ZF), Kris (ECC), Za (Zingo), Jason (ZCG), John (ZF), Arya (ZF)


## Agenda:
- Quick team updates 
- ZIP-320 updates, deployment of TEX addresses coordination
- Open discussion

### ZIP-320 updates
ECC is working on ZIP-320 to support TEX addresses in a way that doesn’t leak any information like the interstitial addresses. The information of these addresses is stored locally on the database. For restoring purposes indices are “reserved” logically following what Bitcoin wallets currently do but under a different child index so they are not used accidentally for other purposes.


Zingo is wrapping up ZIP-317 and is planning to approach ZIP-320 ephemeral 

Updates from Jason and Pacu: other exchanges are no


### Frost Uniffi updates
Pacu is progressing on Uniffi version of FROST for Golang and Swift. Go lang FFI is complete and ready for ZavaX team to review.  

Zingo might be able to contribute with Kotlin bindings for it. 

Pacu was concerned about FROST 2.0 being out anytime soon and that breaking the UniFFI wrapper but Conrado said that 2.0 shouldn’t be hard to adopt. 

### Regtest darkside Zingo Work

Pacu asked Kris about darksidewalletd tests on the ECC SDK and mentioned some shardtree problems.  Za mentioned that Zingo is working on Regtest support as part of Nym integration (Zingo Proxy / Lightwalletd). They want to support darkside RPCs on that Rust implementation of lightwalletd

ECC is also planning to work on fake chain generation on librustzcash crates to be able to test locally without the need of a server. 




