# Light Client Working Group Devs Meeting 100
### Meeting Date/Time: Thursday 24th July, 2025 17:00 UTC

### Meeting Duration: 60 minutes

### Moderators: Pacu (ZecDevRel), Decentralistdan

Attendees: John (ZF), Daira-Emma (ECC), Str4d (ECC), Dorian (Zingo), Nacho (Zingo), Za (Zingo)

### Agenda:

#### Transparent info to be included into the compact block format

This is currently being worked on [this PR](https://github.com/zcash/librustzcash/pull/1781/files)

We reviewed the PR and hashed out some comments

Assumptions / Requirements

- Clients should be able to request that the block header is included.  
  - Currently GetBlockRange does not provide a way for callers to request full block headers for compact Blocks  
- Number of transactions in the block:  
  - Block header is the only piece of information that provides this information.

Next steps:

- Make sure that the PR needs everything it’s needed  
- Make the necessary changes on lightwalletd