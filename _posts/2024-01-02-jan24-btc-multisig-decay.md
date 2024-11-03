---
layout: post
title: "Jan2024-BTC Multi Sig Decay notes"
date: 2024-01-02 23:59:59 -0000
categories: btc multi-sig decay inheritance-planning
author: "Sagun Garg"
tags: btc multi-sig multsig-decay inheritance-planning btc-contracting-key-setup btc-expanding-key-setup
---

# Decaying Multisignature
A 3-of-5 bitcoin multisig that after 60 months decays into a 2-of-5 and after 66 months decays into a 1-of-5. It makes it easy for the user to secure only 5 keys while at the same time allowing the user to lose 4 keys and still recover funds.

Decaying multisig is one of the most interesting features coming out of Miniscript.
e.g. Liana Wallet - https://github.com/wizardsardine/liana

Decaying Multisignature: It enables the user of a multisig wallet to let the threshold decline over time, which means that less private keys are needed after a certain time has passed. When setup properly the user will be able to recover his coins after a certain time(This approach is prominently utilised as a safeguard against the potential loss of funds due to the misplacement of keys.), even if more keys are lost than needed to sign for the quorum. Decaying multisig can help to setup inheritance without the need for a trusted third party (unlike the regular bitcoin inheritance offered today with a trusted third party)

# Setup Trustless Multisignature Inheritance
Decaying multisig can help to setup inheritance without the need for a trusted third party. The owner can give the legatees the threshold minus one key and set that one key will decay after five years. If he upgrades his setup every four years, his legatees will never be able to touch his bitcoins as long as he is alive, because the decay will never happen. If he dies, the threshold will decay with one keys after five years and the legatees can access the bitcoins.

References:
1. https://multisigsigner.com/knowledge-base/features/bitcoin-miniscript/decaying-multisig/
2. https://github.com/wizardsardine/liana




