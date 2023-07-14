# Light Client Working Group Devs Meeting 49
### Meeting Date/Time: Thursday, May 4th, 2023 17:00 UTC
### Meeting Duration: 45 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Lux (Zingo), Adi (Nighthawk) Mandeep (Nighthawk), Matt (Nighthawk), Carter (ECC)
### Notes: Adi

# 1. General Notes
* Changing the way sync status is reported:
  - The current approach of reporting sync status will be revamped.
  - Different stages of download and scanning will be eliminated, and the focus will be on syncing as the download and scanning of blocks happen in parallel.
  - After blocks are scanned, they will be deleted to optimize storage usage.
  - Testing has yielded positive results, indicating the effectiveness of this approach.
  - While there will be some changes in the API, they are not expected to be major.

* Pending tx database removal and improved public API:
  - The pending transaction database will be removed and replaced with a unique identifier system.
  - Previously, it operated as a flow, but the new approach will make the public API much clearer and more streamlined.

* Fixing bugs in transaction history:
  - There will be efforts to address and resolve bugs related to transaction history.
  - This will ensure a more accurate and reliable transaction history for users.

* Enhancing pending database and transaction details:
  - Work is underway to improve the pending database functionality.
  - The aim is to leverage a more precise history and provide detailed information about transactions.
  - Users will be able to view every output between each transaction, including funds sent to self or other addresses.

* Backward compatibility with old protobuf parsers:
  - The new records and changes introduced will still be compatible with older protobuf parsers.
  - This ensures that existing systems relying on the older parsers can still parse and process the new records without issues.

* Introduction of new APIs for instant sync:
  - Additional APIs will be developed specifically for instant sync.
  - These APIs will allow users to retrieve additional data required for achieving instant sync functionality.

* Discussions on upcoming SDK releases and performance improvements:
  - Discussions are taking place regarding future SDK releases.
  - There is a focus on improving overall performance, with tests being conducted to evaluate and measure the effectiveness of these improvements.

* Zingo's plan to integrate new sync code:
  - Zingo has expressed plans to integrate the newly developed sync code into their system.
  - This integration indicates the potential benefits and applicability of the new sync code to other projects or applications.

### Expanded using ChatGPT May 24 Version