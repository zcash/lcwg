# Light Client Working Group Devs Meeting 53
### Meeting Date/Time: Thursday, June 29th, 2023 17:00 UTC
### Meeting Duration: 30 minutes
### [Video of the meeting](not-recorded)
### Moderator: Nick ECC
### Attendees: Mandeep (Nighthawk), Adi (Nighthawk), Matt (Nighthawk), Pacu (Independent)
### Notes: Adi

# 1. General Notes
  - Suggest implementing scan ranges in the ongoing development process.
  - Consider additional states to account for, apart from the ones already considered.
  - Plan to release version 1.0 of the wallet by mid-July.
  - Consider a possible soft launch for Nighthawk Wallet following the SDK release.
  - Investigate the crash in the transaction details view, where the SDK query returned no rows.
  - Address the issue of transactions with null memos.
  - When the synchronizer is scanning, frequently encountered timeout errors should be resolved.
  - Resolve the networking error "DEADLINE_EXCEEDED: deadline exceeded after 89.998219465s" during scanning. Check for closed connections and open connections to "mainnet.lightwalletd.com/140.238.134.157:9067".
  - Assign Adi to open the related issues.
  - Matt should sync up with the latest architectural changes and project module-based changes.
  - Discuss the advantages of merging code changes over cherry-picking to contribute to the same part of the codebase.
  - Focus on implementing Orchard support, starting with the librustzcash backend and then propagating it from there.
  - Explore the feasibility of integrating fiat conversion and third-party APIs.
  - Add custom server settings in the SDK API.
  - Implement a currency API in the Rust layer to facilitate US tax calculations and data persistence to avoid duplication.
  - Pacu will be attending Zcon4 and working independently with Zingo on darkwalletd tests.
  - Similar tests to those done previously for darksidewalletd should be set up, including setting up a regression test, generating blocks with the CLI, extracting information, creating files, and verifying compliance with ZIPs for all wallets.
  
* Useful references for tests:
  - RPC test cache https://github.com/zcash/zcash/tree/master/qa/rpc-tests/cache
  - Golden RPC tests https://github.com/zcash/zcash/tree/master/qa/rpc-tests/golden
  - In ZIP-315 (https://github.com/zcash/zips/pull/607/files), consider including threat models such as lightwalletd leaks.

### Expanded using ChatGPT May 24 Version