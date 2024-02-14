# Light Client Working Group Devs Meeting 69
### Meeting Date/Time: Thursday, February 8th, 2024, 2024 17:00 UTC
### Meeting Duration: 80
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees:  Za (Zingo), Conrado (ZF), John (ZF), Pili (ZF), Kris (ECC), Fluidvanadium (Zingo), Andrew Arnott (nerdbank), Jason McGee (ZCG), Daira-Emma Hopwood (ECC), Str4d (ECC)


## Agenda:
- Team quick updates 
- Update on Binance Exchange Addresses and ZIP-320 implementation across the ecosystem
- Request for input: Preferred approach on ZIP-320


The following items were on the agenda but couldn't be covered:

- Request for input: [DRAFT ZIP: Zcash Wallet Application End of Life / End Of Service Best practices and recommendations](https://forum.zcashcommunity.com/t/draft-zip-zcash-wallet-application-end-of-life-end-of-service-best-practices-and-recommendations/46825)
- Workgroup Initiatives:
  - ZIP-320 implementation across the ecosystem
  - Lightwalletd maintenance and support ZIP-307 / Decentralize Core development


### Presentation Slot: (optional)
None requested.

### Team Updates: 2-3 minute updates per team. Shorter is better
### team quick updates
#### Zingo
Za; Zingo will have an update soon, about collab with ECC on sync. Also working on Lightwalletd and eliminating the go component of the network communication level.

#### ZWCD
Pacu: Currently working on EOS/EOL ZIP and ZIP-320 outreach. Also working on gathering feedback on TEX and UAs from many partners (like EDGE).

### ZIP-320 outreach discussion

**Note:** EDGE's preference on TEXs spinned a discussion on the ZIP-320 outreach that took over the agenda. 
Moderators decided to let the issue be discussed since is the most urgent matter the ecosystem is working on.


Pacu: *Live update*
Just got feedback from EDGE about preferring TEXs. Invited them to give out their feedback on the call.


Daira-Emma: our goal with UA would be reducing protocol complexity and providing secure address encoding that allows readable verification of addresses. The problem of asking around is that we might not be able to make a decision if we get a 50-50 split. We should continue working on UAs until we get good arguments against them and in favor of TEXs, since Binance actually did not give a preference.

Za: Only very technical users care about security properties of different sources.

Kris: There was the point brought up by people about wanting to know the privacy properties of a transaction from the address. 

Str4d: But that didn’t work.

Jason: With going out and getting feedback, the important thing is that we understand their concerns, make sure they don’t bring up issues we weren’t thinking about, and are able to address them if we can. If that means setting up a call to explain to them why we prefer UAs, I think that’s what we should do. It’s not a vote…so even if the majority of this small group we’re going out to prefer TEX addresses, we can still go forward with UAs if we can explain why it’s the better option or if their arguments against it aren’t very strong.


Pacu: Since we are already reaching out, would it be good to actually get partners on a call to get their feedback there instead of asynchronously?

Daira-Emma: *agrees to that*


Kris: if the ecosystem would actually work to get tex address parsing I’d rather them work to support UAs instead

Str4d: considering that multi-coin wallets want to do the bare minimum. Would they want to do any of this work being TEXs or UAs?

Fluidvanadium:  UAs are flexible and we should implement them.

Daira-Emma: let’s not fumble the ball; let’s get this proposal done

Za: if I’m a CEX I’d be worried about becoming obsolete by DEXs. So we could say that UAs can help them to get into a DEX world 

Kris: We need to note that teams are reluctant to adopt FFI stuff, they want native libraries in their language of choice.

Fluidvanadium: we should just implement them, it's not that time consuming.

_Everyone agrees_


Pacu: We will schedule a call next week to gather partners to discuss both approaches. What’s the status of the ZIP-320 work?

Daira-Emma: Work is being done on ZIP-316. HRP for UA rev 2. (will be “ur”)

Fluidvandium: should the wallet say “we need to make funds transparent?”

Daira-Emma and Str4d: not necessary. 2 txs are generated and sent at the same time. Since it’s transparent it is not a problem that the first transaction is not mined.

Str4d: the transparent address should not be internal because funds might be returned so it can’t be internal in the sense of not being shown to the user. Also the returned fund should be shielded before they are spent again. 

Daira-Emma: does it have to be implemented differently than internal change addresses? Because they are the users’ own funds. Probably the wallet should be able to mark these funds as a “refund” and mark them as such in the UI.

Str4d & Kris: this is a perfect case to use memos in internal addresses so that the temporary addresses used are saved in memos so that it can be recorded in the wallet. 

Daira-Emma: Either TEX and UAs will have this 2 tx use case as well. So this shouldn’t matter  to the option that gets implemented.


Andrew, Kris, Daira-Emma and Str4d: discussed the use of diversified addresses and how to manage diversifier indices of transparent, sapling and orchard and  avoiding reuse across the different wallets. It originated this github issue: https://github.com/zcash/zips/issues/781

Str4d: the only thing that matters to restore a wallet is that we can store the deshielding diversifier in the change of the memo field. 

Andrew: as it comes to random diversified indexes there should have to be some rules set up.

