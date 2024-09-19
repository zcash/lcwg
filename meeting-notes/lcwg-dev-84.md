# Light Client Working Group Devs Meeting 84
### Meeting Date/Time: Thursday, September 5th, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @decentralistdan - ECC
### Attendees: Kris (ECC), Za (Zingo), James (Brave), Kyle (brave), ChainSafe, Conrado (ZF)

### Agenda

- Team updates
- How are we doing with problems related to Zebra 1.8.0 tracked on https://github.com/zcash/lightwalletd/issues/497?
- If chainsafe is present, In-Memory Wallet status (https://github.com/zcash/librustzcash/issues/1414) 
- Has there been any progress (material or ideas) about the debate of last meetin on “Restore from seed or restore from wallet file?” https://github.com/zcash/zcash/issues/6873 


Kris(ECC)
- NU6 testnet upgrade 
- back over to wallet side 
  - moving test infra from sql lite to backend 
  - reorg but related to note comit trees in sqlite 

Zingo:
- top priority: implement ZIP320 20th of september 

Chainsafe:
- Webzjs
  - memory backend implementation for librustzcash 
  - forum update
  - chainsafe & kris to talk about serialization async standardizing 
ZF: 
- zcashd depracation 
  - porting RPC tests 
  - overall design 
  - mapping out work 
- FROST
  - working on refresh shares for DKG
- ZEBRA
  - https://github.com/zcash/lightwalletd/issues/497
  - zebra not returning the right call
  - working on fixing the ones that they know cause issues 

Brave: 
- https://github.com/zcash/zips/pull/899
- ZIP drafter (Kyle)


Has there been any progress (material or ideas) about the debate of last meeting on “Restore from seed or restore from wallet file?” 
- https://github.com/zcash/zcash/issues/6873
- from wallet format becasue zcashd has keys not derived from seed  restore from wallet backup

- https://github.com/brave-experiments/hardware-backed-webcrypto
- stalled out on testnet (kris)
  - chainfork or all mining power dropped 
  - conrado looking into it 
