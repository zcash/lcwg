# Light Client Working Group Devs Meeting 51
### Meeting Date/Time: Thursday, June 1st, 2023 17:00 UTC
### Meeting Duration: 45 minutes
### [Video of the meeting](not-recorded)
### Moderator: Nick ECC
### Attendees: Dan (ZF), Mandeep (Nighthawk), John (ZF), Matt (Nighthawk), Adi (Nighthawk), Kris (ECC)
### Notes: Adi

# 1. General Notes
  * ECC restructuring:
    - There has been a restructuring within ECC (Electric Coin Company). Further details or context regarding this restructuring would be helpful to provide more specific information.

  * SDK update and parallelization changes:
    - An SDK update is scheduled for June 12, which will include updates for both Android and iOS platforms.
    - The update will introduce parallelization changes, leading to a significant 30% improvement in speed.
    - More details on the specific changes and improvements introduced in the SDK update would be beneficial.

  * Wallet database migrations and note commitment tree structure:
    - Planned changes to the wallet database will involve altering the structure of how the note commitment tree is stored.
    - These changes will maintain backward compatibility with light clients, ensuring they can still interact with the updated wallet structure.

  * API changes for block scanning and scan updates:
    - The API for scanning blocks will remain the same, but there will be an API change for specifying the next range for linear scan.
    - Suggestions are made to use existing APIs for scanning specific block ranges by requesting the wallet to download those ranges.
    - Additional APIs will be introduced to allow clients to receive scan updates from the wallet backend.

  * Immediate spendability of funds and reverse sync:
    - The goal is to make funds immediately spendable upon synchronization.
    - The preferred structure of synchronization will involve reverse sync, where the wallet syncs from the most recent blocks backwards.
    - This approach aims to provide a better user experience and usability.

  * ZIP-317 and changes to SDKs:
    - ZIP-317 brings changes that enhance usability through the SDKs.
    - More details on the specific changes introduced by ZIP-317 and their impact on usability would be helpful to provide further context.

  * Two-phase transactions and privacy improvements:
    - Two-phase transactions will be implemented, incorporating the changes from ZIP-317.
    - The backend will return a transaction proposal that includes all the necessary instructions to create the transaction, including the selection of relevant notes.
    - Zcash-specific privacy enhancements will be made when transferring funds between pools, considering amounts and fee implications.

  * Nighthawk reported issues:
    - Nighthawk has reported issues, but further information is required to provide specific details via GitHub issue creation.

  * Enhanced functionality for sending funds:
    - There are plans to introduce the ability to send all funds with a query, including notes and total ZIP-317 compatible fees.
    - Changes to the tx proposal API will be necessary to accommodate these enhancements.
    - No specific mention of ZIP-321 transaction requests is made, suggesting it may not be included in the current development focus.

  * Nighthawk modularization and screen visibility:
    - Nighthawk will undergo modularization to maintain a separation of concerns.
    - Older screens will be hidden under a debug menu to streamline the user experience in the v1 version.

### Expanded using ChatGPT May 24 Version