---
layout: post
title: "Arpil22-lightning notes: Blockchain Method of Accounting"
date: 2022-04-12 23:59:59 -0000
categories: notes lightning blockchain method-of-accounting
author: "Sagun Garg"
tags: lightning blockchain method-of-accounting 
---

# My notes on Lightning network Development

1. Lightning Network - payment protocol for utxo-based cryptocurrencies
2. Decentralised network of Lightning nodes (Anybody can run a Lightning Node and join the network anonymously)
3. It difficult to enumerate payee or payer and censor transactions (encrypted transactions)
4. Payments are routed atomically, meaning they either fail in full or succeed. Thus, no trust or preexisting relationship is needed between nodes. Given that, the Lightning Network is considered non-custodial.
5. Lightning Network is made up of nodes and routes (e.g. channels) connecting these nodes.
6. Two nodes can open a payment channel with each other, which will require at least one of them to commit capital in an on-chain transaction. The initially committed capital defines the capacity of the channel over its lifetime.
7. Since it is impractical for everyone to connect to everyone else directly, each lightning node acts as an intermediary thereby working as a routing node for indirect connections for payment rounting and hence can collect a fee.
8. To join the Lightning Network, it is required for either you or your peer to make at least one on-chain transaction.
9. The two parties having a direct channel can then transact infinitely with each other at no cost. But for indirect a payment traverses multiple hops, hence the fee is levied multiple times by each router known in advance.
10. Private/Public Channels - A Lightning Network node is required to send and receive payments in the Lightning Network. However, these nodes do not need to be online permanently. They may be turned on and off at will. Such clients typically use private channels not announced to the larger network. And, they cannot route payments themselves. They can be downloaded as apps or be bundled with other applications.
11. Lightning network payments are designed to be anonymous.
12. You can observe the Lightning Network graph from your own node or from a hosted lightning network explorer
13. To perform a Lightning Network transaction, both peers as well as all routing nodes in between need to be online. For mobile wallets, this often requires keeping the wallet running until the payment is settled, after which the application or device can be turned off.


## Imp. Extra points to note: 
1. The Lightning Network does not have its own token (Instead it uses the token of the underlying network/blockchain)
2. Lightning Network as a “second layer” protocol it uses the base layer only for dispute resolution or to deploy capital into channels.


## Reference: Method of accounting (UTXO or Account based ledger)
1. **UTXO** - UTXO's are not tied to an account, accounts don't really exist in UTXO. It works similar to how cash is handled in your hand amongst friends or family(e.g.Bitcoin, Litecoin, Cardano and NEO)
2.**Account based ledger** - e.g. Ethereum,EOS and Tron uses an 'account' based method. It is much like traditional accounting in that a series of records have to be kept for each and every wallet (user). Literally a digital ledger. As it is account based it functions much like a bank account with a balance. 


## Extra Notes: Design Points of Any new Blockchain
1. Non-custodial: Not your keys, Not your coins - In cryptocurrency, non-custodial systems allow the user to take full control of their funds. This comes at the benefit of having full ownership, but requires the user to manage their own keys (i.e. the saying Not your keys, Not your coins).
2. Method of accounting (UTXO or Account based ledger)