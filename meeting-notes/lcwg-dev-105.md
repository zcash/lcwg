### Meeting Date/Time: Thursday November 13th, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), 

Atendees: Pacu, Za, Matthew Piché (Edge)

Agenda:

- 10 days from NU 6.1: readiness of the light-client ecosystem (All Teams)  
- ~~State of Lightwalletd deprecation (zingo)~~  
- Brainstorming: Next initiatives for LCWG (All Teams)  
  - Zcash React Native SDK initiative

#### 10 days from NU 6.1: readiness of the light-client ecosystem (All Teams)

Matthew is working on Android and iOS integration. Nothing blocking at the moment but Pacu will facilitate if needed. Matthew did notice that their autoshielding implementation should include memos on it but they are not seeing them on the shielding transactions. He will send a code snippet to Pacu so he can help him figure out what’s missing.

#### \[ad hoc\] Zcash React Native SDK

Pacu asked Matthew whether EDGE considered their ZcashRN component for public use or just internal use because lately there have been teams asking about React Native support and there is clearly a gap in Zcash Tooling. Matthew said that it was mostly internal but there have been cases where people asked them things about it so there must be a user or two. Pacu explained a bit the background on this topic where teams like Ledger, Trezor, Atomic, Trust, etc would need a React native SDK to integrate shielded Zcash on their wallets but the ecosystem lacks expertise and support for that stack and that although recently a grant was presented to fill that gap, it was rejected because the team didn’t seem to be able to prove a solid background and past experience and also didn’t propose a production integration of their SDK artifact which risked sustainability and converted the grant in an abstract development. So with this in mind Pacu thought it could be a great idea that Zingo and EDGE partner up as the most React Native knowledgeable teams to start developing this and possibly present a grant application for the project given that they have overlapping requirements but they serve a complimentary public. One is a Zcash only wallet (Zingo) and the other is a multi-coin wallet (EDGE) and could maintain an API that one wallet uses a subset of the features (in this case EDGE would use less Zcash specific features than a Zingo).

Matthew will follow up with Paul on this idea.