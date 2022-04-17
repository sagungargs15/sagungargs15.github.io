---
layout: post
title: "March22-Crypto notes: Bitcoin Smart Contracts"
date: 2022-03-15 23:59:59 -0000
categories: notes crypto bitcoin smart-contracts
author: "Sagun Garg"
tags: crypto bitcoin smart-contracts 
---

***"The Bitcoin community activated Taproot at block 709,632 on November 12th, 2021."***

***"I find blockchain fascinating because it extends open source software development to open source + state. This seems to be a genuine/exciting innovation in computing paradigms; We don’t just get to share code, we get to share a running computer, and anyone anywhere can use it in an open and permissionless manner. The seeds of this revolution arguably began with Bitcoin"*** - [Andrej Karpathy, Director of AI @ Tesla](http://karpathy.github.io/2021/06/21/blockchain/)

# Examples of Smart Contracts on Bitcoin
1. Time Locked Bitcoin Transactions: a script could require 3 signatures to spend the bitcoin before a certain time, after which only 1 signature is required. This makes fallback options possible, ideally preventing a loss of funds. (here time locks can also be used as part of the locking scripts to change the spending requirements of a bitcoin)

## Bitcoin Smart Contracts
1. Pay-to-Public-Key-Hash is one of the simpler Bitcoin smart contracts, but its utility and simplicity make it the most popular
2. Bitcoin’s Taproot upgrade gives Bitcoin users significant flexibility in constructing complex smart contracts on the bitcoin chain (Bitcoin’s Taproot upgrade will introduce a new script type called Pay-to-Taproot (P2TR), which will unite the functionality of P2PKH and P2SH scripts, allowing bitcoin to be sent to both a public key and arbitrary scripts. However, while P2SH and P2WSH allowed bitcoin to be sent to a single script, P2TR uses Merkelized Alternative Script Trees (MAST) to allow bitcoin to be sent to up to 2^128 different, arbitrary scripts. Any one of these scripts can be satisfied to spend the bitcoin.)


## Summary: Taproot Upgrade - Notes
1. Taproot is an upgrade to Bitcoin which introduced several new features (Schnorr Signatures-BIP 340, Taproot-BIP 341, and Tapscript-BIP 342)
2. BIP 340-Taproot integrated the Schnorr digital signature scheme into Bitcoin, upgrading Bitcoin’s core cryptography.
3. BIP 341-Taproot built on the SegWit upgrade to improve Bitcoin’s privacy and lower transaction fees.
4. BIP 342- Taproot made future Bitcoin upgrades easier by reforming Bitcoin’s scripting language.

## References
1. https://river.com/learn/what-is-taproot/
2. https://medium.com/interdax/how-will-schnorr-signatures-benefit-bitcoin-b4482cf85d40