# Light Client Working Group Devs Meeting 95

### Meeting Date/Time: Thursday, April 3rd, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel)

### Attendees: Arlo (Zingo), John (ZF),

### Agenda

- New Shielded Wallet\! Brave\!   
- Darksidewalletd 2.0 tests. Where to implement them, how, who has bandwidth to?  
- Lightwalletd issues ([example here](https://github.com/ZcashFoundation/zebra/issues/9307#issuecomment-2769762821)) how to handle them until Z3 is ready?

We just had a quick meeting. 

On darksidewalletd 2.0:  
\- The objective high level would be to create a Rust crate that implements the proper Zaino traits in a "darkside" way. Bonus points for it being runnable on CI on the same process of the wallet under test.  
\- We have a baseline of tests that Zingolib implements. Those would be good to be checked out by ECC wallet devs. There's probably an intersection between the original tests on the iOS SDK and the ones in ZingoLib, but it's important that we start with small and workable pieces. I understand that Zingoistas are Darkside Ninjas, Monks, Masters, Senseis, etc.

### Homework for next meeting:

\- Pacu: find the notes I had taken when Kris and myself discussed how to go to a Rust implementation of it leveraging librustzcash testing tooling that already exists.  
\- Wallet developers: those interested in integrating darkside tests into their test suites should think of test cases that they would like to implement, from more basic to more advanced. 
