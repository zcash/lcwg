# Light Client Working Group Devs Meeting 38
### Meeting Date/Time: Thursday, November 17th, 2022 17:00 UTC
### Meeting Duration: 30 minutes
### [Video of the meeting](not-recorded)
### Moderator: Pacu Gindre @pacu
### Attendees: Adi @nighthawk24, Carter @ccjernigan
### Notes: Adi

## Decisions and Actions Made
| Item | Description | Video ref |
| ------------- | ----------- | --------- |
| | ||


# 1. General Notes
* General
  - zecpages testnet faucet is down
  - R&D Discord should be used to reach out to core developers
  - A T-address change is expected in wallet, need to educate users.
  - When account [0] address is present, SDK initiates a lookup and then auto shielding when funds are received.
  - Rolling of transparent address is not automatic. It has to be pulled manually.
  - Possible to start adopting the changes with fee field, query for tx, start displaying the fee instead of the constant in Transaction History flow.
  - Friction points to calculate input notes to predict fees.
  - Delays with the SDK release are due to additional changes of fee mechanism ZIP-317.

* Android SDK
  - Android 1.10-beta1 snapshots as pre-release versions are available.
  - New API changes with the ZIP-317 will be followed up in the next release as it requires UI changes in clients.
* iOS SDK
  - SDK release planned for end of November after testing and maybe another one in December.

## Attendees
* @nighthawk24 Nighthawk
* @Pacu ECC
* @ccjernigan ECC