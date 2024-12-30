# Light Client Working Group Devs Meeting 90 

### Meeting Date/Time: Thursday, December 12th, 2024 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), Decentralist (ECC)

### Attendees: Kris (ECC), Za (ZingoLabs), Conrado (ZF)

### Agenda

- Team updates  
- PCZT how to support them in more wallets? Use cases and low hanging fruit.  
- Moving lightwallets from LightwalletD to Zaino how soon can and shall we do it?

**Action Items:**

- Review [https://github.com/zcash/librustzcash/pull/1634](https://github.com/zcash/librustzcash/pull/1634)  
- Open discussion

### PCZT:

- Zec-sqlite-cli was made public today so Pacu could integrate Ledger into that instead of Zingolib.   
- Zec-sqlite-cli might be a smaller bit to munch than Zinglolib, which is a more fully featured wallet.  
- Zec-sqlite-cli can be integrated to Zashi and use PCZT, Pacu will check it out and see if this is possible.

### Lightwalletd to Zaino transition:

- We need the regtest bug on Zebra fixed first to be able to test.  
- Step Zero would be having a Zaino backend by Zcashd but it does entail some work on its own so it might not be worth it.  
- Should be able to just replace 1:1 and test it.

### Librustzcash Forks:

- Zingolib has a well maintained not dangling fork that might be able to be removed and replaced by latest upstream. By that it will enable PCZT usage on Zingo.  
- If Zancas and team can scope out the reason why this fork exists in the first place Pacu might be able to chip in and carry that forward.