# Light Client Working Group Devs Meeting 78
### Meeting Date/Time: Thursday, May 30th, 2024 17:00 UTC
### Meeting Duration: 60 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Kris, Daira, Andrea (ECC), Jason (ZCG), Conrado (ZF), Fluidvanadium (Zingo)

## Agenda:
- Quick team updates 
- ZIP-320 updates 
- ZIP-315 call for review https://github.com/zcash/zips/pull/607
- Imminent lightwalletd.com public infrastructure shut down
- Progress Cocoapods Support for ECC iOS SDK
- Open discussion


### ZIP-320 updates

Go lang to be audited by LA.
Go zcash_address crate port module were sent to coinbase for review request for comment
ZIP-320 support on ECC SDKs is still in development. 
Zingo TEX address support relies on transaction proposal from librustzcash.

https://github.com/zcash/librustzcash/pull/1257

### ZIP-315 call for review
Call for review. Daira-Emma intends to merge as draft soon and open issues for outstanding todo’s.

Spreadsheet with requirements that Pacu had put together https://docs.google.com/spreadsheets/d/1oGIrts5wJ8eduhIwIo7i1Qb0IR8E1YCjosg7RidT1M4/edit?usp=sharing

### imminent lightwalletd.com public infrastructure shut down
ZCG and ZF have not been able to contact NH about doing DNS forwarding of the domain. But there is uncertainty around whether that would work because it could be the case that the TLS certificate chain fails when the zec.rocks server responds. 



### Open discussion
#### CURRENCY CONVERSION for Zashi, LWD and privacy concerns
Retrieving the currency conversion from the provider leaks the IP and other related metadata.
Possibilities to implement:
Sign up to a provided that provides signed data that LWD can relay that info to the wallets
LWD to act as TLS proxy to connect to providers to get exchange rate 

In terms of historical data rates could be stored in change memo outputs.

#### FROST server demo.
Pacu asked about the progress on the FROST server to use it in the PoC. Conrado replied that they will be adding it to the demo soon. 


