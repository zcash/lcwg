# Light Client Working Group Devs Meeting 97

### Meeting Date/Time: Thursday, May 15th, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel)

### Attendees: Matthew (EDGE), Oscar (Zingo) Decentralistdan (ECC), Nuttycom (ECC), John (ZF),

### Agenda

Remove T-addresses from UAs




#### Remove T-addresses from UAs
How to roll this out? New revision or just removing them and not accepting them?

Is the prefix important?  

Daira-Emma and Kris think that the prefix is not important but Conrado proposes 
that the prefix is Z 

**Are there any breaking changes to the existing APIs for ECC SDKs?**

- It is because callers are getting the T address from the UA   
- There could be a deprecation cycle.  
- The other option is for the current method to return a ZU address without any changes but that would be difficult to do because the ZU would use address rotation and currently SDKs don’t.


Changes needed in other libraries:
- ZIP-312 libraries?  
- Zcash\_address would need changes.

**How do we communicate this so it’s not understood as “deprecating t-addresses”?**


kinds of Address names present in apps:
- Zingo k: Orchard | Complete | Z-Sapling  
- EDGE: “Your Unified Address (shielded)” | “Your Sapling Address” | “Your Transparent Address”  
- Ywallet:  Main | Diversified | Orchard | Sapling | Transparent  
- Zashi: Shielded | Transparent


Possible names?
- ZU address (Daira-Emma)  
- Have the shielded concept around (conrado)

Are there any backward compatibility issues that might have to be dealt with?
- just the API breaking changes  
- This works as UA revision 1 was intended.   
- There would be a runtime error to attempt to generate a UA revision 1 with a transparent receiver.


Oscar: Is jumble related to hiding information for the user?

No, it indirectly does that but the goal is to make similarity/reproduction attacks possible


About displaying to users, it’s ok to display its capabilities to users. Currently shielded wallets ignore transparent receivers so it’s not an issue that UAs have them at the moment. Is about addresses you give out.

Action Items:

- PR for UA rev 1 (ECC) and reviewers needed (everyone\!)  
- ZIP-316 changes (ZIP Editors) and reviewers needed (everyone\!)  
- User Facing Name for the ZU types? Where should they go?  
  - There should be **no** new name. Just Zcash or Shielded Address should do.