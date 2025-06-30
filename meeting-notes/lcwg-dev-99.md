# Light Client Working Group Devs Meeting 99
### Meeting Date/Time: Thursday 26th June, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), Decentralistdan

Attendees: alamode (zingo), arlo (zingo), Za (zingo), nacho (zingo), Kris (ECC), 

Agenda:

- OpenRPC no other updates than what’s present in Zallet’s repo at the moment  
- Deprecating Lightwalletd  
  - Maintain the same API for the time being.  
  - There’s a reorg bug on zaino around cached state that should be fixed and that will be considered “a proper replacement”   
  - What’s the process we should put in place once this is achieved?  
    - Start hosting new servers  
    - Signal Lightwalletd repo to point people to Zaino as official light client server  
    - NU7 could be a milestone where we could tilt people over to Zaino away from Lightwalletd  
      - Kris thinks that Lightwalletd should continue to serve parts of the protocol that are still valid for NU7 that are not part of NU7.  
      - Za: we should avoid different versions of light wallet protocol implementations to coexist like   
- Z3 RPC method information redundancy problem  
  - Having Based the RPC’s from the bitcoin RPCs there are some fields that are we don’t want replicate like validateaddress (which shouldn’t exist at all)  
  - The problem of not supporting existing flat structures is to break compatibility with existing clients, if it were to be some breakage the approach would be to actually break everything into new structures  
  - Nacho suggested layering the architecture so that there’s a compatibility layer to make these compromises that serves the flattened representation and then Z3 clients actually benefit from rich types and semantics that makes sense.  
  - There’s currently a problem with reusing data types across the ecosystem where coexisting libraries in a single project (through dependencies) cause problems and undesirable rigidity on those types where changes can’t be made without breaking other parties’ code. What’s the level of independence we want on each level of Z3?  
  - all of the types that there are protocol encodings defined for (like addresses and transactions) are the most future-proof, we could actually add metadata to it for versioning.   
  - What are the parts of librustzcash that are mapped to the protocol or network upgrade that could be assumed to have assurances of not being changed between upgrades? Zcash\_protocol could be but actually there could be changes that are not tied to network upgrade but maintainers haven’t set their opinions on which one is the right approach.  
  - Zaino RPCs are being implemented with the Zcashd C++ code as reference, there are definitely differences between readthedocs and the code that have been there forever and that have been also discovered during zallet development, the rule of thumb is to document them by opening an issue in github and bringing it up in development groups.  
  - Shall we build a new spec doc (“now yes, please, read the docs”)?  
  - There are definitely tensions on this existing RPC interface given its pre-existence and tech debt contributions, Zaino actually has a milestones of getting rid of the legacy RPC interface, so it could be that this flattened vs rich types discussion is nonsensical   
  - If we were to build a new RPC interface using gRPC then we could set a rational set of types we could represent in this new spec that are served on this new interface and then not needing to maintain any of the rest that we consider legacy or transitional 