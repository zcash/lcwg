# Light Client Working Group Devs Meeting 74
### Meeting Date/Time: Thursday, April 4th, 2024, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Eric Tu (chainsafe), Jason (ZCG), John (ZF), Kris (ECC), Za (Zingo), Cypt4 

## Agenda:
- Quick team updates 
- Status update: development, outreach and deployment of Binance "transparent-source only t-addresses" and ZIP-320 implementation across the ecosystem
- adoption and use of new LWD infrastructure RFP granted by ZCG
- [META] LCWG calendar
- Open discussion!


### Meta LCWG Calendar
Next LCWG Pacu will be OOO, so he won't be able to moderate and take notes but he encourages others to take the lead and hold the meeting anyway!.


### Zcash Js/TS feasibility study from chainsafe

Eric:
They are researching what the next steps are for Js/TS wallet application, Standalone Extension or Metamas Snap. 

Each one of them has pros and cons. For example Metamasks have limitations in terms of spinning up multiple threads and storage limit of 100MB.

They have a metamask snap embedded benchmark. 

They are closely following the zcash_client_backend crate to know how much of it they can reuse because of differences on how the javascript / wasm environment executes tasks. 

Kris: they are interested in hearing these requirements from them because they would be open to implement an executor kind of approach in the crates so that the clients can actually chose whether they use an async or sync execution.There’s an unknown in the development effort needed but they would appreciate a team that contributes upstream top-down changes. Starting by shardtree would mean that everything has to change.

Za: Oscar from Zingo might have an async version of shardtree that he used on the BlockStore trait.

Eric: there are other questions as for example the sqlite crates and them not being really compatible with wasm. 

Kris: There’s an effort from ZF engineers to  make an in-memory version of the backend that might help creating a set of components that help with these sqlite coupling storage issues. 

###  ZIP-320 implementation across the ecosystem
Pacu: Jason and I have been reaching out to different transparent wallets and exchanges with regards of ZIP-320.  

Kris: in terms of shielded support for mobile SDK, there’s been work from Daira in terms of handling one-use-only t-addresses as source for TEX addresses. This hasn’t been picked up by Kris since many team members are on OOO. It should be expected that this could be worked on end-of-april. There’s some demand from users saying that the z->t transfers are being rejected from some recipients so it would be good to get in touch with them to know more about it and include them in the outreach.

Pacu: provided we have ways to contact them we will.

Kris provided a link to the conversation in question. 

Za:  ZIP-320 might not make it to the next release of Zingo; they'll be aiming for the release after that one. 

Kris. there’s some bottleneck in PR review capacity so there are things that would be good to have reviewers for. 

Jason: Least Authority could help with that. 

Kris: handed over the link that Pacu will share with them. 
