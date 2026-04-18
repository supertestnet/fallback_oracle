# Fallback oracle
A POC for oracle-based betting contracts with an optional simple majority vote by the oracles

# What is this?
This is a webpage where you can create and execute a bitcoin smart contract with a bunch of interesting properties involving oracles. I'll tell you more in a second.

# How can I try it?
Just click here and follow the instructions: https://supertestnet.github.io/fallback_oracle/

# What is interesting about this smart contract?
Several things:
- The smart contract will be between two parties, Alice and Bob
- They will be betting on the outcome of some future event
- 10 oracles will adjudicate the bet by saying Yes if the future event happened or No otherwise
- If Alice and Bob agree on the outcome, the loser sends their private key to the winner, and the winner sweeps the funds immediately, without needing information from the oracles
- If they disagree on the outcome, the winner can sweep the funds immediately using a simple majority vote from the oracles: Alice can sweep if 6 out of 10 oracles said Yes, and Bob can sweep if 6 out of 10 oracles said No
- If most of the oracles went down, the winner can wait a week and then withdraw as long as at least 1 oracle spoke up and no other oracle disagreed
- If all of the oracles went down, either party can wait a week plus 90 minutes and then divide up the funds 50/50 between one another

# Why did you make this?
I was talking to someone about developing an oracle-based application on bitcoin and he opined that it might be a pain to use oracles in a bitcoin context. I had him describe the oracle system he'd like to see for bitcoin, which was pretty similar to what I built here, and then I built it over the course of a few days. Now I'm putting it online so I can send him the link and get his feedback.
