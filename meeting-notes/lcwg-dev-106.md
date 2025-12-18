### Meeting Date/Time: Thursday December 11th, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), 

Atendees: Dorian, Oscar, Za (Zingo), Diego (StackWallet), Paul (EDGE), Kris, Larry (ECC), 

## Notes:

### Zcash React Native Support (EDGE and Zingo Labs)

- Paul’s idea:  
  - One grant/effort to optimize ECC sdk and get rid of bottlenecks  
    - See “Refactoring ECC SDKs to eliminate tech debt” below  
  - Another grant to maintain an official RN SDK,  
- Zingo use of React Native on mobile  
  - Zingo uses react native on zingo mobile which they interface to zingolib as zcash backend   
- Zingo’s use of React on Zingo PC for desktop

### Zcash Flutter Support (Diego from StackWallet)

- Flutter SDK is needed for StackWallet and others like cake wallet who wanted to integrate Zcash but couldn’t because there’s not tooling   
- Diego’s team has been sketching out a document to present a grant on it. They’ll present a draft of their requirements for the rest of the group to look at async around new year. 

### Sync speeds:

#### Refactoring ECC SDKs to eliminate tech debt

Thinning the ECC SDKs

- Paul will get a spec they have (pre 2019\) for the API they need   
  - [https://gist.github.com/paullinator/c37efc137f50fd7e11e6e4ffca7b0a94](https://gist.github.com/paullinator/c37efc137f50fd7e11e6e4ffca7b0a94)  
- Come up with a better light API.   
- This needs to actually move the networking layer out of the Swift and Kotlin sides  
- Also stop using the SQL db as middleware for the Native and Rust sides of the FFI.   
- This will entail that the Swift and Kotlin parts of the SDKs are mostly a shim that call on operations happening on the rust side, which will increase code reuse and remove a lot of duplicate logic.   
- Also  a great opportunity to redefine public APIs. 

Current stack used at Zingolabs:

- Desktop: zingolib with node bindings generated through [neon-rs](https://neon-rs.dev/).  
- Mobile: zingolib with Swift and Kotlin bindings generated with [UniFFI](https://mozilla.github.io/uniffi-rs/latest/).

### Pepper-sync as zcash\_client\_backend implementation?

There will be a walkthrough call tentatively on December 16th 14.00 UTC where Oscar will show attendees their way around pepper sync. This call will help us see how to better integrate pepper-sync into the librustzcash tooling and start having a more integrated approach in terms of syncing algorithms.

Zingo is planning to present a grant on this and they need input from Kris, so this call will help both ways. 