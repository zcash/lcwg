# Light Client Working Group Devs Meeting 86
### Meeting Date/Time: Thursday, October 3rd, 2024 17:00 UTC
### Meeting Duration: 50 minutes
### Moderators: Pacu (ZecDevRel), Decentralist (ECC)
### Attendees: Kris (ECC), Eric (ChainSafe), Za (Zingo)

### Agenda

- Team updates
- If chainsafe is present, In-Memory Wallet status (https://github.com/zcash/librustzcash/issues/1414) 
- ZIP 320 statuses towards Sept 20th.
  - Zingo
  - ECC SDK client wallets (Nighthawk, Unstoppable, Edge)
- Status of Partial transaction format for Hardware wallets and FROST


### Team updates

- Team updates  
- iOS 18 updates\! Heads up\!\!  
- If chainsafe is present, In-Memory Wallet status ([https://github.com/zcash/librustzcash/issues/1414](https://github.com/zcash/librustzcash/issues/1414))   
- ZIP 320 statuses towards Sept 20th.  
  - Zingo  
  - ECC SDK client wallets (Nighthawk, Unstoppable, Edge)  
- Status of Partial transaction format for Hardware wallets and FROST


Chainsafe:
- Wrapping up the in memory wallet cleanup.  
  - Wont’ merge the code until the zcash client backend is hardened a bit.   
    - On ChainSafe’s side they have to abstract their code to have less repeated code with the zcash\_client\_backend sqlite code.   
    - Theres a lot of glue code that make librust zcash code “serde serializable”.  
    -   
  - Working on test cases   
- In browser wallet  
  - Working on PoC Wallet so that they can tighten the Javascript API  
    - They can sync and send transactions  
    - Still managing the KeyManagement aspect.  
    - The snap team will be joining these calls when they start working on it  
- ECC:  
  - The problem of defining serialization is that it is forever. So there needs to be a clear separation between serialization and how the data is represented.   
  - The boiler plate code is useful and we wil discuss it on a separate meeting  
  - New Shardtree version will ship with changes and fixes in reorg handling. Read the release notes\!  
  - From Nuttycom:  
    - The one major thing that people in the ecosystem should be aware of is that the \`shardtree\` crate will have a new release in the next few days. This includes some important changes to the API and changes in semantics in the \`ShardStore\` interface; people should read the CHANGELOG for the next release carefully: [https://github.com/zcash/incrementalmerkletree/blob/main/shardtree/CHANGELOG.md](https://github.com/zcash/incrementalmerkletree/blob/main/shardtree/CHANGELOG.md)  
    - The changes here are to restructure some APIs that were not well-aligned with how the crate is used in wallets. The old APIs had some behavior that could result in note commitment tree corruption if they were not used carefully and in potentially non-obvious ways, so this is an important upgrade. I apologize for the disruption; the problematic APIs had been a result of a bad API decision long ago (the API was designed even before the \`bridgetree\` crate was written) and it's been a thorn in my side the whole time, so when misuse resulted in note commitment tree corruption in Zashi that was the final straw.  
    - Also note that the \`bridgetree\` crate is now EOL with the exception of bug fixes; no new features or other changes are planned for that crate  
- Zingo:   
  - They are progressing on ZIP-320 and having a rough time with tech debt from ZecWallet code. OscarPepper is actually working on a new keystore. 