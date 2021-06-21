# secretballot
Ethereum smart contract to conduct a secret ballot vote (commit/reveal election).

This Solidity contract was written for a university assignment, and facilitates secret ballot elections/polls using a commit-reveal scheme. In such a scheme, an election/poll is conducted in two phases:
1. ***Commit phase***. First, voters each make their choice and create a password. Each voter combines their voting choice with their password, hashes the result, and submits it. 
2. ***Reveal phase***. After the commit phase (which can be time-limited for example), every voter who committed a vote previously now gets to reveal their choice so that all of the votes can be counted. To do this, one must submit their voting choice and their secret password in plaintext. These are then combined and hashed, and if they match a vote commit submitted in the commit phase, then the vote is counted.

The contract as yet does not have a front-end, and currently only the owner can create ballots to vote on (with only one ballot taking place at a time). In the future these issues may be addressed to provide a tidy showcase of my Solidity and web3.js skills 😉.
