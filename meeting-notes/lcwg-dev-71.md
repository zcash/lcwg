# Light Client Working Group Devs Meeting 71
### Meeting Date/Time: Thursday, February 22nd, 2024, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Conrado, John, Kris, Conrado, Jason McGee, Paul (EDGE)


## Agenda:
- Quick team updates 
- Discussion: development, outreach and deployment of Binance "transparent-source only t-addresses" and ZIP-320 implementation across the ecosystem


## ZIP-320 outreach

Kris: Binance told us that they don’t support any kind of external library and that actually makes the UA approach not feasible (at the moment). ECC is working on several PRs to support for ZIP-320 on zcashd, librustzcash and the ECC SDKs

Jason: what’s the timeline for this since Binance needs to know when to roll their side of the changes. We don’t want them generating TEX addresses without other wallets supporting them

Kris: the Zcash address crate will be complete in around a week supporting TEX addresses. Zcash wallet support is not planned. The ECC SDK release will be end of march because there are other features being released as well like orchard support.

Pacu: what’s the expected path for transparent zec wallets to implement TEX addresses?

Kris: they would need some sort of library or way to parse the TEX address.

Jason: maybe Paul from EDGE can expand

Paul: we do support shielded wallets but if we treated ZEC as bitcoin we would need a way to make the code understand the address and then everything else would actually work.

Kris: For EDGE and other SDK based wallets the change would be smaller with one caveat because there are 2 tx returned instead of one.

Pacu: What's the best order to roll all the stuff out? 

Kris: other partners can do how they please with the parsing. Transparent wallets can just implement their parsing part immediately. We don’t know what Zingo or Ywallet will do with the economic actions of spending.

Jason: what does the exchange have to do if the user wants to send to binance? Or from binance?

Kris: to send from binance will be the same as usual. If other exchange ideally we don’t want anyone to generate 
 
Further questions for partners:
What kind of languages do they need UA support for?
Who uses Zcashd wallet?

Paul: key languages Typescript, Swift and Kotlin native implementation.

Pacu: has ECC talked with Zenith developers?


Dan: posted this link https://nextcloud.vergara.tech/index.php/s/WqtWs6rGZKMCjr
ECC: no we haven't. 

Pacu: Has ZF ?

Conrado: not yet.

Jason: when will ZIP-320 be published?

Kris: We'll meet with Daira and do the adjustments soon.

Jason: I want to contact Binance and update them so they are up to speed.

Dan: Za just joined

Za: we will support whatever is needed to support parsing TEX addresses. What’s the timeline from binance?

Jason: they haven’t given a timeline or deadline.

Za: we can have a release done two weeks after the code is ready 


Paul: will there be a beta release? Our developer that works on Zcash takes a leava at the end of march.

Kris: yes, but android is a bit behind.

Paul: EDGE is a react native app so it needs both. 

## Call to action:
- Paul: will contact their devs to join next meeting to talk about dependency management with cocoapods
- Daira and Kris: Finish ZIP-320
- Pacu: send comms about finalized zip, adjust ZIP-321 and 315 drafts
- Jason: get Contacts from some partnerds for Pacu to reach out. Contact Binance with latest updates.
