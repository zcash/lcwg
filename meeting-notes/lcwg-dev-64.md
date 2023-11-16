# Light Client Working Group Devs Meeting 64
### Meeting Date/Time: Thursday, Nov 2nd, 2023 17:00 UTC
### Meeting Duration: 40 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Zooko (ECC), Kris (ECC), Danyul (Chainsafe), John (ZF)
### Notes: @pacu

## Agenda:
- LCWG and Daylight Saving Time observation
- Team Updates

## General Notes

### DST and LCWG
Arborist call hasn't been moved nor discussed being moved around DST changes. So this will be considered around that change.


### Chainsafe updates: 
- no particular updates on their behalf. They are willing so meet with ZCG and move the grant forward.


### ECC Update
- Exited Emergency Mode 
- Zashi beta testing on-going
- orchard support developmen started!
- moving github repositories from zcash to electric-coin 
- ZcashLightClientKit will be moving to a new name `zcash-swift-wallet-sdk`
- zcash-light-client-ffi will be moved under `zcash-swift-wallet-sdk` its release
process will be changed to github releases to avoid repository bloat.
- Librustzcash is undergoing some structural changes around how the codebase is being
split into creates to improve the ergonomics of the APIs

### ZF Updates

John: Zebra external wallet is working with ECC scanning tooling. 

Kris suggested that
Zebra engineers and ECC engineers get together to get feedback on the rust creates being
used.


### ZWCD Updates
Pacu is starting the Office Hours as estipulated on the ZWCD grant, a meet the Zavax bridge team. 
**Reorg tests and other tooling:**

Finished building Advanced Reorg tests on Zingo and moving on to other wallets.

There's a limitation on the ECC SDKs which is the lack of REGTEST support that he can contribute to but needs input from ECC's Core Team to iron out some technical decisions. 
According to Kris, PR would be much welcome. Although, ligthwalletd support is under consideration. It has not been considered a priority by ECC and according to Zooko, they won't dedicating any resources other than the essentially to support Zashi, their flagship wallet.

ZF anf ZCG should be made aware of this so it can be brought up to the wide community since
lightwalletd infrastructure is used by many actors around the ecosystem (see action item).

**ZIP-321 support for mobile**:


next milestone of ZWCD allocates time for supporting ZIP-321 request for nighthawk and other native apps. There are some doubts around input validation and dependency loops that can be
created if there's native library importing the Zcash SDKs to validate addresses while wallet applications import both the ZIP-321 library and Zcash SDK. 

Kris suggested that address validation, although is optional by the ZIP, could be achieved by
using `zcash_address` crate over the ffi. 

Decentralistdan also mentioned that there could be an opportunity to leverage the zcash-uniffi library from Eiger. 


### Actions Items for next call
- Bring up Lightwalletd codebase maintenance and support as an ecosystem issue
