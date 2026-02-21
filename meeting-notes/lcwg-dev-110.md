### Meeting Date/Time: Thursday February 19th, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), 

Atendees: Torn, Mikel (Decentrathai), Kris, Larry (ZODL), Dismad

## Agenda:

- Flutter SDK:   
  - Nyms from Decentrathai (z.chat) and mrhaydari are developing one. How can we combine all of these efforts?  
  - Z.chat uses the Zcash chain as transport. They were based on Zashi and created a message first.  The problem is that memos don’t have forward secrecy so they would need [https://zips.z.cash/zip-0231](https://zips.z.cash/zip-0231) to be implemented. Decentrathai folks should continue to build their app but also work to get the zip included in NU7  
  - Pacu will send a PR to that ZIP to add use cases of his. Decentrathai folks will communicate their requirement on the forums  
- React native SDK:  
  - Cocoapods platform is winding down. How does that impact EDGE’s SDK? No quorum  
- All of the lightwalletd changes for transparent data have merged.  When can we make a release of Lightwalletd?   
  - There are many PRs opened recently  
    - Those were vibecoded and need further inspection so will be left out the next release  
  - We will cut a release with transparent data \+ some other small PR.