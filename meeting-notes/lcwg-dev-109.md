### Meeting Date/Time: Thursday February 4th, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), 

Atendees: Dorian, Za (Zingo), Diego, Josh (StackWallet), Kris, Larry (ZnewCo)

## Agenda:

- Action Items from last call  
- ~~React Native SDK: Kickstarting this effort after Holiday break. Appointees: EDGE, ZingoLabs~~  
  - ~~CocoaPods: Press F for respect. Are we ready to move to SPM? What’s needed?~~   
- Flutter SDK: CakeWallet integrated Ywallet, what can we learn from it? Appointee: Diego from StackWallet  
  - Some Nym from the forums just showed up with this dart sdk-ish [https://forum.zcashcommunity.com/t/introducing-zcash-dart-a-dart-library-for-zcash-transactions-zero-knowledge-proofs/54561](https://forum.zcashcommunity.com/t/introducing-zcash-dart-a-dart-library-for-zcash-transactions-zero-knowledge-proofs/54561)  
  - Diego from stack wallet got a collaborator interested in integrating Zcash.  
  - Cakewallet sdk may be an opportunity but it seems that it’s not the final solution for cake wallet.  
  - A dev from stackwallet was exploring Zcash inclusion and will get back at us with what’s needed for integrating Zcash into Dart (flutter) wallets.  
    - He developed a PoC Rust wallet. He realized that Zcash would be easy to integrate   
  - The problem is that they have feature parity with their desktop wallet and they can’t use it. They support MacOS, Linux and mobile.  
    - They use Cbindgen and Rust.  
    - This probably    
- ~~Lightwalletd and Prometheus support? Is it being used? What do we need to implement on Zaino? What metrics shall we gather?~~   
- Zcash SDKs will move back into the Zcash org   
- LWD will start rolling out releases with transparent data.  
- ZeWIF: Kris will get back to that next week.   
- ZexCavator: a zip is needed to describe all of the key derivations used by wallets over time.   
  - [https://hackmd.io/@daira/rJVEmOCkh](https://hackmd.io/@daira/rJVEmOCkh)

## Action Items:

- ZeWIF key derivation ZIP: Dorian will start to draft a ZIP with key derivation from ZecWallet which he is currently looking at as a starting point  
- Rotating t-addresses  
  - Kris needs to get the in-flight pieces in librustzcash for t-address rotation   
    - This implies changing the sync algorithm as well to account for those rotated addresses  
  - FFI and SDK integration  
- PRs worth looking into:  
  - Zcash dev tool has a PR for FROST integration   [https://github.com/zcash/zcash-devtool/pull/137](https://github.com/zcash/zcash-devtool/pull/137)  
  - Extensible transaction format ZIP draft: https://github.com/zcash/zips/pull/1156