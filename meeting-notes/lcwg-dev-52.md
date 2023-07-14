# Light Client Working Group Devs Meeting 52
### Meeting Date/Time: Thursday, June 15th, 2023 17:00 UTC
### Meeting Duration: 45 minutes
### [Video of the meeting](not-recorded)
### Moderator: Nick ECC
### Attendees: Lux (Zingo), Mandeep (Nighthawk), Adi (Nighthawk), John (ZF), Matt (Nighthawk), Bernard (Chainsafe)
### Notes: Adi

# 1. General Notes
 * Configurable lightwalletd in SDKs:
  - The question arises regarding the placement of the lightwalletd server in the SDKs. Should it be implemented on the client or server side?
  - Considerations need to be made regarding allowing configuration options for the LCWG within the SDKs to provide flexibility to developers.

 * Direct light clients to the chain:
  - To enhance the functionality of light clients, the goal is to establish direct connections between them and the Zcash chain.
  - For sending transactions, the aim is to reach the zcashd node directly via the mixnet.
  - However, when it comes to receiving information, it's important to assess the performance of lookups. Focus should be on lookups that require privacy, such as transaction information, rather than downloading entire blocks.
  - Latency involved in the mixnet might not be feasible, especially considering the need for dagsync to enable random access chain sync. It's important to utilize bandwidth that scales for end-client wallets.

 * Bug fix for iOS:
  - Matt is currently working on fixing a bug related to iOS. More details about the bug and its resolution would be helpful to provide further information.

 * Sapling scanning issue and recent SDK release:
  - There is a known issue related to sapling scanning that requires some work to make changes to the SDK. This task is expected to take approximately another week or two to complete.
  - The most recent SDK release has shown improvements, including parallelization code and bug fixes.
  - The sapling scanning process has been optimized, and it now takes around 10 hours to complete.

 * Medium-term considerations:
  - Orchard pool support is a question that needs to be addressed in the medium term.
  - Fast sync and minor changes to the SDK are also part of the plan for future development.
  - Orchard spend functionality should be explored as well.

 * Zingo Labs and Orchard support:
  - Zingo Labs has submitted a pull request (PR) related to Orchard support, specifically PR 582.

 * Architecture and tools:
  - The provided link showcases the Zcash Core DAG (Directed Acyclic Graph) and its dependencies at the bottom of the graph.
  - ChainSafe is mentioned in the context of the project or its architecture.
  - Snaps is described as an extension system for MetaMask, and relevant links are provided.
  - It's unclear if the architecture is based on Ubuntu snaps. Further clarification is needed.

 * Persistence layer and related resources:
  - The usage of a persistence layer is recommended. Further details on the specific implementation or its benefits would be helpful.
  - The provided link leads to a summary related to Milestone 5 in the context of uniffi-zcash-lib on GitHub.

 * Zcash xchain.js wallet and testnet workflows:
  - The Zcash xchain.js wallet is suggested as a reference for development using TypeScript.
  - The provided link directs to a testnet block explorer that can be utilized for testing and validating workflows on the testnet.

### Expanded using ChatGPT May 24 Version