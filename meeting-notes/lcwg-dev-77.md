# Light Client Working Group Devs Meeting 77
### Meeting Date/Time: Thursday, May 16th, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Kris (ECC), emersonian (zec.rocks), Matias (Testnet Infra grant author), Andrea (ECC), John (ZF), Jason (ZCG), Conrado (ZF), 


## Agenda:
- Quick team updates 
- ZIP-320 updates 
- ZIP-315 call for review 
- imminent public Infrastructure changes on May 30th

### ZIP-320 updates
Wednesday night we some Zcash devs had a conversation with Binance devs about TEX address implementation. Binance required a specific RPC method to be implemented on Zcashd for them to be able to make TEX address deposits to be available in production. Kris Nuttycombe opened a PR against the Zcashd repo for that. There is a mandatory cross-reference check Binance developers have to comply in order to release TEX address support on their end but they hadn’t stated it as such previous to this last conversation

Binance is withholding deposits from Zcash shielded wallets and imposing a 31 business days parking prior they can be returned to their recipient. It is not clear that we can actually talk with them to make that shorter. They did update their applications to show an alert about shielded deposits to users generating QR codes on their site and apps. Zingo has proposed to inform the users in the shielded wallets as well but it’s unsure if that messaging will be confusing to the rest of the users sending to a t-address that is not from binance and could confuse users more than helping them. Zashi will not implement such messaging until they hear from their users.


### ZIP-315 call for review
This PR is under review. We will call the wide community of wallet developers to review the comments Daira-Emma and other co-authors are doing to that ZIP draft so that we can generate a feature matrix that can provide better guidance for developers and users on which features to support and how to support them.


### imminent public infrastructure 
A private and public ecosystem outreach was carried out by Pacu about this. Also Emersonian stated that he will be putting up infrastructure for a Block Explorer using  NightHawk’s ZBE open source repos. Emersonian said that he was not able to find the docker piece that supported the “send raw transaction” feature of ZBE. But Pacu advised to listen to the Legal and Regulation talks on ZconV before enabling such a feature. 

Matias, who is proposing a grant on Testnet and Production testing infrastructure presented himself. Part of his grant is making a block explorer that supports Zebra. Kris actually said that ZF and ECC engineers are actually working out in a layer of data that will support various indices on a DB for transparent features of the protocol and ultimately for block explorers and tol Matias to be around those discussions in discord to make sure the requirements for a block explorer are included. 

Pacu invited Matias to today’s arborist call at 2100 UTC.


### Open discussion

Pacu is wrapping up the FROST rust crates and enabling features to recreate the Zcash demo in swift and other languages and invited others to review the rust code and make suggestions.