# Light Client Working Group Devs Meeting 89 

### Meeting Date/Time: Thursday, November 14th, 2024 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), Decentralist (ECC)

### Attendees: Kris (ECC), Conrado(ZF), John (ZF), Za (Zingo)

Light Client Working Group \#89 is tomorrow (Thursday)

Where? Jitsi [https://meet.jit.si/moderated/f941f58ae8dfe97138f74e55436508f6fa0523eb5f70494b47ec31494e524980](https://meet.jit.si/moderated/f941f58ae8dfe97138f74e55436508f6fa0523eb5f70494b47ec31494e524980)

### Agenda

- Team updates  
- ~~Latest lightwalletd issues~~  
- ~~How’s working on Kubernetes and Dockerized infra?~~  
- PCZT and TX Building: how can we help move that forward? (development and testing)  
- Librustzcash upgrade paths for light clients. How to get everyone to the latest crates?  
- Open discussion

### PCZT and TX Building: how can we help move that forward? (development and testing)

Is possible to test this PR [https://github.com/zcash/librustzcash/pull/1577](https://github.com/zcash/librustzcash/pull/1577)   
Postcard format will be used for versioning. There’s no need for migration but agreement on schema is needed. 

Transaction builder refactor is here: [https://github.com/zcash/librustzcash/pull/1477](https://github.com/zcash/librustzcash/pull/1477)

What’s needed for FROST? 

FROST does not specifically need anything in particular included in v1. Once PCZT is included in librustzcash the FROST team can work out the details to include that feature in the signing tool that’s on the demo instead of relying on Ywallet’s transaction plan. 

### Librustzcash upgrade paths for light clients. How to get everyone to the latest crates?

Kris, Str4d and Daira have to decide a time to put together the librustzcash walkthrough. That will likely happen in a Zoom webinar which will be recorded.   