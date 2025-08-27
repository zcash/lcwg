### Meeting Date/Time: Thursday 21st August, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), Decentralistdan

Attendees: John, Kris 

### Agenda: 

#### work on https://github.com/zcash/librustzcash/pull/1781 and next steps

Currently both ECC and Zaino folks are overloaded, what can be good strategies to advance this without disrupting the team's flow?

- This is not blocking on anything on the Zcashd deprecation critical path so this can be delayed until zaino folks have more bandwidth or file a grant to do this work

#### In-memory Zcash client backend implementation

Steps to merge the in-memory Zcash client back end implementation, Ledger's retroactive grant is greatly impacted by this at a "risk" level  
	\- this is actually a blocker on Zcashd deprecation because Metamask needs to be able to get updates to the protocol for NU 6.1 

#### Transaction parser RFP:

Pacu should get the following information from exchanges prior to the RFP to be drafted:  
\- How do they parse Zcash transactions?  
\- When a Zcash network upgrade requires transaction changes, what work needs to be done on your side? How can we make that easier for you?  
\- If you use your own parser, how can the Zcash community help your organization to maintain that parser?  
\- there’s going to be two transaction format changes early next year, how can we make this easier? 
