# Light Client Working Group Devs Meeting 58
### Meeting Date/Time: Thursday, Aug 24th, 2023 17:00 UTC
### Meeting Duration: 40git minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: @nuttycom (ECC), John (ZF), Mandeep Bhalothia (NH), Conrado (ZF), Aditya 
### Notes: @pacu

## General Notes

### NH Updates 
Matt couldn't make it but sent update through signal:

Lukas and him were working on Updating the FFI version NH was pointing to. Changes that Lukas suggested are working, but Matt will still need one of our testers who was running into problems to test the PR and verify in his end, since he was unable to repro the issue himself. 

NH iOS team just wrapped up implementing sync notifications feature. PR is up for review. They are moving through the rest of the backlog items.

### Outreach for ZIP-317 adoption
One of the pressing issues besides the effects of sandblasting, is mempool congestion. This is mostly caused by the transactions taking out all the "free actions" of each block, but also because of wallets not adhering to and implementing ZIP-317 fees. This not only affecting shielded wallets. All wallets that use transparent ZEC are being affected too. In the arborist call it was proposed that there's an ecosystem outreach to wallet developers of all sorts (HW, Shielded, Transparent) to make them aware of the new fee ZIP and direct them to resources on how to implement it.

As Pacu mentioned on the arborist call earlier, there are two parts of the Ecosystem Outreach: one is the person-to-person outreach that's acknowledged (or not), and then the async follow-up when the point of contact relays to their development team the actions to fulfill the outreach's requests. The latter entails teams having to assess and prioritize the work that needs to be done to fulfill the outreach's request. The best way this is to be successful is for the Zcash developer community to make comprehensive resources available to minimize misunderstandings, lower the partners' implementation efforts and risks and to avoid unnecessary two-way communications between ZIP-317 implementors within the different teams and the Zcash developers and ZIP editors


### ZWCD Updates
Pacu is working in darksidewalletd benchmarks for Zingo that will be extended and made available to other wallets. Also reviewing PRs from NH and ECC. 

He requested suggestions on improving regtest performance because the testcase generation was taking too much time and had to move on to a different approach.

For this Kris pointed out [this code](https://github.com/zcash/zcash/blob/master/qa/rpc-tests/test_framework/util.py) that could help set up cached regtest states and then use the resulting wallet directory to generate the darksidewalletd datasets.

In terms of organizing LCWG Pacu and Decentralistdan have been working to get the Zoom call venue ready for today's call. Additionally Pacu is reaching out to all development teams that had previously participated on LCWG to invite them over and get feedback and their preferred times in an attempt to accomodate everyone better. 


### ECC Updates

#### SDKs pre-release testing 

Kris mentioned that testing of the SDKs would be appreciated, clients of the sdk should check [zcash-wallet-dag](https://zcash.github.io/developers/zcash-wallet-dag.svg)

Zooko: announcing taking on roles EM and Product for SDKs
on [this post on the forums](https://forum.zcashcommunity.com/t/all-ecc-teams-focused-on-wallet-performance/42860/107?u=zooko)

ECC plans to ship SbS capable SDKs once Str4d is back. No other changes will be done in terms of mitigating mempool congestions issues. 

LCWG discord channel users wanting to join the Zashi beta testing program might message Zooko


#### Darksidewalletd Testing and Sbs 
Kris: There are Darksidetests that need review and fixing on the SDKs on [This PR](https://github.com/zcash/ZcashLightClientKit/pull/1191). Pacu will review and prioritize any work if possible since there are other tasks in his backlog.

Kris also suggested that the Dlwd tests have a definition language so that tests can be written once and ran on whichever wallet and those tests suites can be user on z.cash to actually get it listed on the official wallet list on the website.

https://github.com/zcash/ZcashLightClientKit/pull/1191


###  Action Items from previous meeting
- ~Enable ZIP-317 booleans on the sdk and do small releases~. This has been deprioritized by ECC to focus on Sbs. Minimum fee of 10000 zat may or may not be included in next release.


### Action Items from this meeting
- @decentralistdan representing ZF and @pacu as ZWCD will get together to shape up the ZIP-317 outreach. Any technical follow-ups needed with ECC's core team will be channeled through Zooko.