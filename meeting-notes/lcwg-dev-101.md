### Meeting Date/Time: Thursday 7th August, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), Decentralistdan

Attendees: Kris (ECC), Arlo (Zingo), Daira-Emma (ECC), 

### Agenda:

#### Transparent info to be included into the compact block format

This is currently being worked on [this PR](https://github.com/zcash/librustzcash/pull/1781/files)

Shall we move out from gRPC? No, “gRPC is the worse rpc framework except for all the rest”

Next steps for handling .proto files

- Create a zcash/lightwallet\_proto repository,  
- Move the canonical protofiles from lightwalletd there  
- Make a PR with git subtree or submodule to pull them back 

The idea is that we don’t implement this feature in lightwalletd at all and we do it in Zaino instead.

#### Merge of in-memory zcash\_client\_backend PR:

This ball has been on our court for a while and it’s gaining relevance as continuation of the metamask snap continues and [WebZ.js](http://WebZ.js) is adopted in other projects we will likely need to merge it to main.

Next steps:

- Kris will recap on the state of the PR and see what is its path to the `main` branch. We will assess whether he can initiate the structure of that work and hand it over to Pacu for completion.