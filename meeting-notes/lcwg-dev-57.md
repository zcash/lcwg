# Light Client Working Group Devs Meeting 57
### Meeting Date/Time: Thursday, Aug 17th, 2023 17:00 UTC
### Meeting Duration: 30 minutes
### Moderator: @pacu - ZWCD
### Attendees: @nuttycom (ECC), John (ZF), Matthew Watt (NH), Mandeep Bhalothia (NH), Conrado (ZF), @str4d (ECC), Aditya 
### Notes: @pacu

### 1. General Notes
#### Mempool growth and transaction eviction issues
- Adi is getting reports from users of different wallets about transactions not going through
- Str4d says the problem might be related to transaction expiry heights not being set properly or
ZIP-317 not being enforced properly. Recommended expiry height is 40 blocks since Blossom. If a transaction is stuck
- Reports on graphana show that the mempool started to grow up in size within the previous 15 days. One workaround would be shrinking the mempool size on nodes, setting expiry heights and enforcing ZIP-317 fees.
- According to NH team, the mempool is being fully populated with small transactions with small amount of actions and the blocks are barely including any of them, therefore causing user txs
being unmined and expired.

Pacu: What actions that can be taken to avoid workarounds and get the concrete solutions out?

Kris: 
- Review and get void out for the changes of transaction proposal here: https://github.com/zcash/librustzcash/pull/891
- Create Swift and Android implementations of ZIP-317 so that apps can parse the proposals made by librustzcash
- Enable the ZIP-317 boolean flag on the SDK blindly without a transaction proposal. 

#### ECC SDKs:
**Fast spendability (Spend Before Sync):**
- About new releases, the team hopes that bugs are solved when the outstanding PRs are closed and the wallet SDKs will be released the following week (Aug 21-25). these new releases might include basic support for ZIP-317 fees.
- There's an outstanding matter about displaying balance in terms of spendability. There could be cases where users are using the same seed on different wallets and the SDK detects notes that have been spent but that's unknown until the block is fully scanned. Currently, ECC Team assumes that the keys are not being used in other wallets to determine spendable balance.
- Adi: can the user spend while syncing? Str4d: Yes, the SDKs will support spending while syncing.

**ZIP-317 Fees:**
- Transaction proposal API that allows fees to be pre-calculated before sending will follow up in a second release from the one mentioned above.
- Mandeep reports that the Android SDK is not showing up fees for received transactions. The issue has been reported by Matt and Pacu but has not been looked at yet. 

**DAG Sync:**
- currently there's no timeline for DAG sync and it will be moved to work to the ZF and ECC collaboration on making Zebra the main node implementation.

**Darksidewalletd**:
- bugfixes implemented on the lightwalletd but tests on the iOS SDK are still buggy.

**Action Items:**
- Enable ZIP-317 booleans on the sdk and do small releases. 
Related Links:
- https://github.com/zcash/zcash-android-wallet-sdk/blob/main/backend-lib/src/main/java/cash/z/ecc/android/sdk/internal/jni/RustBackend.kt#L362
- https://github.com/zcash/ZcashLightClientKit/blob/main/Sources/ZcashLightClientKit/Rust/ZcashRustBackend.swift#L14

