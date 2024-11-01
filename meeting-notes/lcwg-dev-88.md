# Light Client Working Group Devs Meeting 88 

### Meeting Date/Time: Thursday, October 31st, 2024 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), Decentralist (ECC)

### Attendees: John (ZF), Conrado (ZF), Kris (ECC), Za (Zingo), Arlo (Zingo)

### Agenda

- Team updates  
- FROST in mobile, what’s needed?  
- Keystone and Ledger in Mobile. What’s missing?  
- Light client brainstorming  
  - What shall we work on next?  
  - What are the gaps between Zcash and other wallets?  
  - WebZ: Zcash in the Browser. How to make it worth it? 

FROST in mobile, what’s needed?

- Server is almost ready but how to start the   
- How to present the FROST wallet in the wallets  
- Guidelines on how to run the FROST protocol in practice. Maybe a ZIP

Zaino RPC for lightwallets

- [Agree on LightWallet gRPC Services to be Deprecated.](https://github.com/zingolabs/zaino/issues/70)  
- [Agree on transparent tx service for wallets](https://github.com/zingolabs/zaino/issues/71)  


Light client brainstorming

- How to encourage people to use UAs?  
- More tooling approach.  
- Taxing older pools?

Keystone and Ledger in Mobile. What’s missing?

- PCZT PR   
- Orchard Support for Ledger  
- A framework that decouples Ledger Usage from the wallets.

Light client brainstorming

- WebZ: Zcash in the Browser. How to make it worth it?   
  - \[idea\] Metamask key based authentication to services?

Can Zingo add a backwards compatible addition to ZIP-307 for adding transparent data to the compact block model so that Larry can implement it on lightwalletd?  
That’s currently not planned on their roadmap.

ECC is leaning towards considering Lightwalletd adversarial where no transparent information is requested in a way that the server can learn the IP address.  Zingo has made quite some work on that

Action items

- List of deprecated RPCs  
- Send this to Snap team at chainsafe [PCZT](https://github.com/zcash/librustzcash/pull/1577)  
- Review this. [Lightwalletd return errors fix](https://github.com/zcash/lightwalletd/pull/503)  
- Add getblock to outreach https://getblock.io/nodes/zec/
  Point them to the tooling that Yassed did for dockerized infra