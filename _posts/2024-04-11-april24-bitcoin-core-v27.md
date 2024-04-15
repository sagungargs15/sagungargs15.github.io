---
layout: post
title: "Arpil24-BTC New Bitcoin Core v27.0 Release"
date: 2024-03-11 23:59:59 -0000
categories: bitcoincore release Libitcoin mempool BIP
author: "Sagun Garg"
tags: bitcoincore release technical improvements Libitcoin mempool BIP324
---

# Bitcoin Core 27.0: Refining the Foundations of Bitcoin

The upcoming release of Bitcoin Core version 27.0 represents a significant step forward in the evolution of the Bitcoin protocol's core software. Underlying this release are several technical improvements that aim to enhance the stability, security, and usability of the Bitcoin network.

One of the notable changes in Bitcoin Core 27.0 is the deprecation of the Libitcoin consensus library. This library was an earlier attempt to extract the core consensus rules of Bitcoin into a separate module, allowing other software projects to leverage the fundamental rules without the full weight of the Bitcoin Core codebase. However, maintaining this library proved challenging, as the complexities of the Bitcoin consensus rules made it difficult to fully encapsulate them. The decision to remove Libitcoin in favor of the emerging Bitcoin Kernel project reflects a recognition that a more comprehensive and sustainable approach is needed to facilitate interoperability between different Bitcoin software implementations.

Another key enhancement in this release is the improvement to how the mempool, the pool of unconfirmed transactions, is managed. When a Bitcoin Core node is shut down, the mempool is now saved to disk and restored upon restart, ensuring that previously known transactions are not lost. This feature helps to streamline the node's synchronization process and improves the overall user experience. However, it also introduces a potential challenge, as some virus scanning software may incorrectly identify the mempool file as a security risk due to the inclusion of transaction data. The developers have addressed this issue by implementing a lightweight encryption scheme to obfuscate the mempool contents, mitigating the risk of false positives.

The default enablement of BIP324 (Developed by Dhruv Mehta, a Bitcoin Core developer, and building on the work of Jonas Schnelli, BIP 324, https://github.com/bitcoin/bips/blob/master/bip-0324.mediawiki), which provides end-to-end encryption for network connections between Bitcoin nodes, is another significant security improvement. By encrypting these connections, Bitcoin Core 27.0 enhances the privacy and integrity of the data exchanged between participants in the network, making it more difficult for third parties to eavesdrop or tamper with the information flow.

These technical refinements, along with other minor adjustments, demonstrate the ongoing commitment of the Bitcoin Core development team to strengthening the foundations of the Bitcoin protocol. As the ecosystem continues to grow and evolve, these incremental improvements play a crucial role in ensuring the long-term stability and resilience of the Bitcoin network.

# Summary: Main Updates

    1. Deprecation of the Libitcoin consensus library, which was an attempt to extract the core consensus rules into a separate library. This is being removed in favor of a new project called Bitcoin Kernel.

    2. Improvements to how the mempool (unconfirmed transactions) is saved and restored when restarting the Bitcoin Core node. This helps preserve the mempool across restarts, but introduces a potential issue with virus scanners identifying the mempool file as suspicious.

    3. The default enablement of BIP 324, which adds encryption to network connections between Bitcoin nodes.

    4. Removal of the "network adjusted time" feature, which used to adjust a node's internal clock based on time information from peers.

    5. Disabling of external signing support for hardware wallets on Windows, which may impact some users.

    6. Introduction of a new coin selection algorithm called "Coin Grinder" that focuses on minimizing fees for high fee environments, even if it's not optimal for the long-term health of the wallet's UTXO set.
