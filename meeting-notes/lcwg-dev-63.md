# Light Client Working Group Devs Meeting 63
### Meeting Date/Time: Thursday, Oct 19th, 2023 17:00 UTC
### Meeting Duration: 40 minutes
### Moderator: @pacu - ZWCD, @decentralistdan - ZF
### Attendees: Zooko (ECC), Danyul (Chainsafe), John (ZF), Matt (NH)
### Notes: @pacu

## Agenda:
- LCWG and Daylight Saving Time observation
- Team Updates

## General Notes

### DST and LCWG
Mandeep from NightHawk requested if it was possible to move this call an hour earlier. I responded that
we would have to check whether there were any conflicts with other calls given DST changes next month.
The group will discuss impact on DST on the different attendants and reconvene a new schedule if needed.

### NightHawk Updates
Ran into some issues:
- when importing from seed where all memos are gone.
- Outgoing transaction is breaking because the only recipient is the internal address. 

Matt opened an issue for the first problem reported: https://github.com/zcash/ZcashLightClientKit/issues/1306

### ECC Update

ECC will be releasing 2.0.3 with bug fixes and feedback provided by partners. Kris and Str4d are out this week.

Follow-up on item from last meeting:
> Zooko: Next call ECC will be sharing Plans for their next Term. Also asked people wanting to be in the beta testing of Zashi to reach out to him or Kris. 

ECC is working on a Blog post to share its plans for next term shortly.

### ZF Updates

John: not much updates, been working on FROST and Zebra tasks

Dan: NYM Grant proposal has been presented throught ZCG's submittable platform . Wallet integration is planned for Zingo and NightHawk accorting to their submission. It would be good for the NYM integration team to join these calls.

Pacu: Agrees that they join, at least to the discord group to discuss networking integration specifically on native
 apps that leverage the ECC SDKs which have particular network settings. 


### ZWCD Updates
Pacu is starting the Office Hours as estipulated on the ZWCD grant, already met with Chainsafe and is planning to 
also meet the Zavax bridge team. Also is building the Advanced ReOrg Test tooling and integrating it to Zingo.
There's a limitation on the ECC SDKs which is the lack of REGTEST support that he can contribute to but needs
input from ECC's Core Team to iron out some technical decisions.

Zooko: suggested that Unstoppable and Edge are invited to these calls. Pacu will send invites to them again. 


### Actions Items for next call
- Sort out daylight saving time conflicts 
- Invite NYM, Unstoppable and Edge