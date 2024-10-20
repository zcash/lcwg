# Light Client Working Group Devs Meeting 87
### Meeting Date/Time: Thursday, October 17th, 2024 17:00 UTC
### Meeting Duration: 50 minutes
### Moderators: Pacu (ZecDevRel), Decentralist (ECC)
### Attendees: Kris (ECC), Za, Conrado, Arlo, John (ZF)

### Agenda

- Team updates  
- Status of Partial transaction format for Hardware wallets and FROST  
- ZIP 320 statuses towards   
  - Zingo  
  - ECC SDK client wallets (Nighthawk, Unstoppable, Edge)  
- WebZ.js wrap up: pending items, blockers, future development  
- What can LCWG do help with Zcashd Deprecation  
- [Meta] Grants resulting in dangling forks of zcash libraries. How to avoid them? 

### Team Updates

Zingo: working on zip 320\. Should have that out by next week

PCZT: review this pr [https://github.com/zcash/librustzcash/pull/1577](https://github.com/zcash/librustzcash/pull/1577)

- What can LCWG do help with Zcashd Deprecation  
  - Get fleshless skeleton of the new wallet application of the wallet server  
  - API Design  
  - Middleware to plugin different platforms  
  - Open PRs  
  - Patch the holes of missing functionality 

ECC: 

- There’s a new addition that supports change management. [https://github.com/zcash/librustzcash/pull/1579](https://github.com/zcash/librustzcash/pull/1579)

Pacu: would this enable creating notes of arbitrary sizes that might help bridge crossing more anonymously?

- Yes this would help, but it has to be noted that the note composition is known to the wallet and might not be an issue for bridge crossing given the user inputs the amount they want and note management won’t matter, except for the 1 note problem 
