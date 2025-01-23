# Light Client Working Group Devs Meeting 92 

### Meeting Date/Time: Thursday, January 23rd, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), Decentralist (ECC)

### Attendees: Pili (ZF), Conrado (ZF), Kris (ECC), Arlo (Zingo), Zancas (Zingo)

### Agenda

- FROST: Which Zcash wallet will be the first one to implement it? What do we have, what are we missing?  
- Darksidewalletd 2.0: A new testing infrastructure for wallets.  
- ~~Collab question from ZingoLabs to Brave. How does Brave Shielded wallet access chain information? Do you plan to use shielded memos for somethings? How can we collaborate?~~  
- Memo Bundle implementation  
    
  


### FROST: Which Zcash wallet will be the first one to implement it? What do we have, what are we missing?

ZF will host a community call to show the new work on FROST and also the Dev Summit in Sofia will be a good time to get devs together to work on requirements for it. Tentative date for FROST Code Walkthrough is the first Week of February. 

BC folks are interested in advancing FROST and would like to attend that walkthrough

### Darksidewalletd 2.0: A new testing infrastructure for wallets.

Kris and Pacu worked together in the Z|ECC summit to think of a new darkside testing that uses Zaino RPC interface to serve synthetic blockchains. This could be either a module inside of Zaino or a standalone crate that just implements an interface/trait of Zaino to provide lightwalletd interface \+ added methods for darkside. 

### Memo Bundles:

Str4d and Kris got together to design memo bundle APIs that will be handled through PCZTs because it makes that available to HW wallets and FROST. Kris has a draft implementation of it. 

### Action Items:

Review needed  of Gap Limit implementation for Transparent wallets. [https://github.com/zcash/librustzcash/pull/1673](https://github.com/zcash/librustzcash/pull/1673). 

Pacu wants Zingo to bring up the delta of its Librustzcash fork so that those differences can be ironed out and Zingo can be updated to the latest crates. Kris and zingoista OscarPepper will pair up on that.

Librustzcash codewalk: what’s the UTC band of people on LCWG?

Organize Librustzcash \<\> Zingo call