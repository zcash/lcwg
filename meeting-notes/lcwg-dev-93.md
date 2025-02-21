# Light Client Working Group Devs Meeting 93

### Meeting Date/Time: Thursday, February 6th, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), Decentralist (ECC)

### Attendees: Conrado (ZF), Daira-Emma (ECC), Kris (ECC), John (ZF), Dorian (Zingo), Za (Zingo)

### Agenda

- \[Meta\] augment scope of these calls, record them and publish them.   
- Preparing for ZeWiF: what do we have to do?  
- ZSAs: From Zcash wallet to a shielded multi-asset wallet. Approaches, suggestions and ideas on how to transition to that.   
- Open discussion.  
  


### Action Items from last call:

* Review needed of Gap Limit implementation for Transparent wallets. [https://github.com/zcash/librustzcash/pull/1673](https://github.com/zcash/librustzcash/pull/1673).   
* Zingo: bring up the delta of its Librustzcash fork so that those differences can be ironed out and Zingo can be updated to the latest crates. Kris and zingoista OscarPepper will pair up on that. Did they?   
* Librustzcash codewalk: what’s the UTC band of people on LCWG?

### \[Meta\] augment scope of these calls, record them and publish them. 

According to Kris there’s no need to formalize this meeting more. Grantees should start attending 

### Preparing for ZeWiF: what do we have to do?

- Move zcashd conf to configure Zallet.   
- The implementation idea was to have everything integrated to ZexCavator  
- The reference implementation will be separate. 

### ZSAs: From Zcash wallet to a shielded multi-asset wallet. Approaches, suggestions and ideas on how to transition to that. 

- Asset description field will be a hash of the description    
- There will have to be a common approach for wallets to register an interest in a particular asset. There should be a repository that provides an issuer key and asset description that can be checked against the hash in the asset description field.  
- How does the user get a decentralized source of information about whether they can trust some issuer and asset?  
- If the recipient receives a payment but does not have knowledge of having to whitelist (allowlist) an asset, what would happen then?  
- There’s transaction controls proposed [https://forum.zcashcommunity.com/t/introducing-transaction-controls-in-zcash/49640](https://forum.zcashcommunity.com/t/introducing-transaction-controls-in-zcash/49640)  
- Transaction controls wouldn’t solve the problem of having to trust that the issuer is who it is.  
- There could be a site that receives opinions of people on that asset but it’s a moderation problem.  
- The minimum viable solution could be that the user goes to the issuer’s site and registers the ID of the asset that it’s interested in.  
- IDEA: zBloc votes could be used as a way to allowlist tokens