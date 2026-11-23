---
layout: post
title: "Nov2026 - IF P = NP IS SOLVED | Bitcoin's Proof of Work in a World Where Hardness Vanishes & Why Quantum Upgrades Won't Save It"
date: 2026-11-22 23:59:59 -0000
categories: bitcoin p-vs-np proof-of-work cryptography
author: "Sagun Garg"
tags: bitcoin p-vs-np proof-of-work cryptography quantum-resistance bip-360
---

## The P versus NP Question
P versus NP is one of the seven Clay Mathematics Institute Millennium Prize Problems, carrying a $1 million prize. It asks a deceptively simple question: if a solution to a problem can be **checked** quickly (in polynomial time), can it also be **found** quickly? Problems whose solutions can be found quickly form the class **P**; problems whose solutions can be verified quickly form the class **NP**. Every problem in P is also in NP. Nobody has proven whether the reverse holds.

![P vs NP Euler diagram: on the left (P ≠ NP), Bitcoin's PoW nonce search and ECDSA key recovery sit in NP but outside P; on the right (P = NP), both collapse into P](/assets/images/2026-nov-blog-post-sanfrancisco-p-vs-np-bitcoin.jpeg)
*Figure: Where Bitcoin's two hard problems sit. Under P ≠ NP they lie in NP but outside P. Under a practical P = NP, both collapse into P.*

Bitcoin's entire security model is a bet that, for the problems it uses, finding is vastly harder than checking. This post walks through what happens to Bitcoin if P = NP is ever solved in the affirmative, where things actually stand as of November 2026, and why the post-quantum upgrades now being drafted protect against one threat but not the other.

## Where P vs NP Actually Stands (November 2026)
Before the thought experiment, a reality check. **P versus NP remains unsolved.** No claimed proof in either direction has been accepted by the complexity theory community.

**A steady stream of unverified claims:** 2026 has seen numerous self-published "proofs" on arXiv, Zenodo, engrXiv and preprint servers, claiming both P = NP and P ≠ NP. None has survived expert review. In one June 2026 episode, an advertised Lean 4 "machine-verified" proof of P = NP turned out, on inspection, to have defined its top-level proposition as simply `True` in its first version, later revised to an uninterpreted axiom. Formal verification only helps if the theorem being verified actually states what it claims to.

**Expert outlook:** Complexity theorist Lance Fortnow wrote in June 2026 that he does not expect to see P vs NP resolved in his lifetime, by humans or machines, even given recent advances in AI-assisted proofs.

**The closest real development - ETH under challenge:** On October 26, 2026, OpenAI announced that its AI system had found a slightly sub-exponential algorithm that would contradict the **Exponential Time Hypothesis (ETH)**, a 27-year-old assumption that NP-complete problems like 3-SAT require truly exponential time. Anthropic reportedly announced a related result. Russell Impagliazzo, Ramamohan Paturi and Ryan Williams are organizing a community review and have stated their involvement is not a certification. Critically, **refuting ETH would not imply P = NP.** ETH is a much stronger claim than P ≠ NP; "slightly faster than exponential" is still nowhere near polynomial. But it is a reminder that long-held hardness assumptions can be revisited.

## Key Properties of Proof of Work Relevant to P vs NP
Bitcoin's Proof of Work depends on a foundational asymmetry:

**The Puzzle:** Miners must find a nonce such that the double SHA-256 hash of a block header falls at or below a network difficulty target.

**Easy to Verify:** Checking a candidate block is a single double-SHA-256 computation, essentially instant on any device.

**Hard to Find:** No known shortcut exists. Miners brute-force the search space, and the expected number of attempts scales directly with difficulty.

**Difficulty Adjustment:** Every 2,016 blocks, the network retargets difficulty so that blocks arrive roughly every 10 minutes, regardless of how much hash power joins.

**Economic Security:** Because valid blocks are expensive to produce, rewriting history requires out-spending the honest network. This cost is what makes confirmations meaningful.

This "easy to check, hard to find" structure is exactly the shape of an NP search problem.

## Why Proof of Work Breaks Under a Practical P = NP
If someone produced a **constructive, efficient** algorithm for NP search problems, the asymmetry Bitcoin relies on would collapse.

**Block Production Becomes Nearly Free:** Finding a valid nonce would no longer require meaningful computational work. Mining would stop being a proof of anything.

**Difficulty Adjustment Becomes Irrelevant:** Raising the target only makes brute-force harder. It does nothing against an algorithm that solves the puzzle directly.

**History Becomes Rewritable:** The cost of reorganizing recent blocks or dominating block production would fall dramatically, enabling double-spends.

**Signatures Fall Too:** Recovering a private key from a public key (the elliptic curve discrete logarithm problem behind ECDSA and Schnorr on secp256k1) is also an NP search problem. Coins could be stolen outright, not just double-spent.

**Incentive Alignment Fails:** The game theory that keeps miners honest assumes honest mining is the most profitable use of expensive hardware. That assumption disappears.

Scott Aaronson put it bluntly in a lecture at Los Alamos: someone who proves P = NP should first "steal $200 billion in bitcoin," then solve the remaining Millennium Prize Problems.

## Why It Might Not Matter: The Three Escape Hatches
The doomsday scenario requires a very specific kind of proof. Three outcomes would leave Bitcoin largely untouched:

**1. A Non-Constructive Proof:** A proof that P = NP exists without exhibiting the algorithm. Donald Knuth has argued that such a proof will almost surely be nonconstructive. A proof of existence mines no blocks.

**2. Impractical Polynomial Degree:** An algorithm running in n¹⁰⁰ time is technically "polynomial" but would be slower than brute force for any real input size. Complexity classes describe asymptotic behaviour, not the cost at n = 256 bits.

**3. P ≠ NP:** The outcome most researchers expect. Bitcoin's assumptions are confirmed rather than broken. (Strictly, P ≠ NP alone does not prove SHA-256 is hard, but it removes the general shortcut.)

The concerning scenario is narrow: a **low-degree, constructive** algorithm for NP search. That is the case the rest of this post addresses.

## The Nearer-Term Threat: Quantum Computing and BIP-360
While a practical P = NP remains improbable, quantum computing is receiving far more engineering attention, and it threatens Bitcoin very differently:

**Signatures Are the Weak Point:** Shor's algorithm can, in principle, derive private keys from exposed public keys on a cryptographically relevant quantum computer (CRQC). This breaks ECDSA and Schnorr.

**Mining Is Mostly Safe:** Grover's algorithm offers only a quadratic speedup for hash search. That would shift mining economics but is offset by difficulty adjustment. Quantum computers are not believed to solve NP-complete problems efficiently.

**BIP-360 (Pay-to-Merkle-Root / P2MR):** Assigned in December 2024 and merged into the official BIP repository in February 2026, BIP-360 proposes a new SegWit version 2 output type (addresses starting `bc1z`). It is modeled on Taproot but removes the key-path spend, so no public key sits exposed on-chain until coins are spent through the script path. It is still in **Draft** status, and a repository merge does not signal endorsement or activation.

**What BIP-360 Does Not Do:** It does not itself introduce post-quantum signatures. Its authors describe it as a foundation for follow-on soft forks.

**BIP-361 and Signature Candidates:** A companion proposal outlines phased migration and eventual sunset of legacy signature schemes. Candidates include lattice-based ML-DSA (Dilithium), the more compact FN-DSA (Falcon, pending FIPS 206), and hash-based SLH-DSA (SPHINCS+) as a conservative fallback. All are significantly larger than today's 64-byte Schnorr signatures, creating block-space and fee trade-offs.

**Testnet Progress:** BTQ Technologies released a Bitcoin Quantum testnet (v0.3.0) in March 2026 implementing P2MR with ML-DSA signature opcodes, the first functional validation of the design.

**Satoshi's Contingency:** In 2010, Satoshi Nakamoto described a plan for hash-function breakage: if weakness appears gradually, the network can migrate to a new hash function after a predetermined block height; a sudden break would require agreeing on the last honest chain before continuing under the new function.

## Why Quantum Upgrades Don't Solve the P = NP Problem
This is the key distinction. Post-quantum cryptography swaps one hard problem (discrete logarithms) for others (lattices, hash preimages) that quantum computers are not known to solve efficiently. Every one of those replacements is still an NP problem.

**Swapping Hash Functions Buys Nothing:** Any puzzle that is easy to verify becomes easy to solve under a practical P = NP. A new hash function inherits the same fate.

**Post-Quantum Signatures Fall Too:** Lattice and hash-based signature forgery are NP search problems. P2MR outputs would be no safer than legacy ones.

**A Deeper Redesign Would Be Required:** The network would face a fundamental choice about consensus models that do not rely on computational hardness at all: hybrid designs, social or economic finality mechanisms, or explicit acceptance of weaker security assumptions.

**Information-Theoretic Security Doesn't Scale:** Schemes like one-time pads remain secure regardless of P vs NP, but they require pre-shared secrets and are impractical for an open, permissionless public ledger.

## Mathematical Breakdown
### Current (2026):
Expected hashes per block ≈ difficulty × 2³²

Verification cost: 2 SHA-256 computations (constant)

Implication: The finding-to-checking cost ratio is astronomically large, and that ratio *is* Bitcoin's security budget.

### Under Grover (Quantum):
Search cost falls from roughly N attempts to roughly √N

Countermeasure: Difficulty adjustment, plus the enormous practical overhead of quantum hardware. Quantum miners would compete, not dominate by default.

Implication: Mining is **degraded, not broken.**

### Under Practical P = NP (degree k, small):
Search cost falls from roughly 2ⁿ to roughly nᵏ, where n is the input size in bits

Countermeasure: None within Proof of Work. Raising difficulty adds bits to n, which grows polynomially, not exponentially.

Implication: Mining is **broken, not degraded.** The ratio between finding and checking collapses toward one.

### Under Impractical P = NP (e.g. n¹⁰⁰):
At n = 256: 256¹⁰⁰ = 2⁸⁰⁰ steps, far worse than brute force on a 2²⁵⁶ space

Implication: A theoretical earthquake with **no practical effect** on Bitcoin.

## Lessons from Stablecoin Regulation
In my [May 2025 post on the GENIUS Act](/stablecoins/regulation/genius-act/us-treasuries/2025/05/02/stablecoins-genius-act-us-treasuries.html), I argued that clear reserve and transparency rules would turn stablecoin issuers into structural buyers of U.S. Treasuries. A similar dynamic applies here: clear, activated rules for quantum-resistant outputs could channel custodians, exchanges and long-term holders toward upgraded address types, much as SegWit and Taproot moved from optional to widespread. The same risks carry over too: incomplete or rushed upgrades leave gaps, compliance-style costs favour large players, and coins whose public keys are already on-chain (including early, unmoved coins) remain exposed until migrated.

## Risks and Open Questions
**Migration Inertia:** Users must actively move coins to new address types. Lost or dormant coins cannot migrate, raising contentious questions about whether exposed coins should eventually be frozen.

**Fee Pressure:** Larger post-quantum signatures consume more block space, raising transaction costs.

**Timeline Uncertainty:** There is no consensus on when a CRQC might arrive, which makes urgency itself a point of debate.

**Hardness Assumptions Are Assumptions:** The ETH challenge of October 2026 shows that assumptions held for decades can be questioned. Bitcoin's security ultimately rests on expert belief, not proof.

## Conclusion
Bitcoin's Proof of Work is **not safe** against a practical, constructive, low-degree solution to P = NP. Neither are its signatures, and neither are the post-quantum replacements now being drafted. The network's present security depends on the widely held expert judgment that such a solution either does not exist or will never be usable at cryptographic scale. As of November 2026, that judgment stands: P vs NP remains open, dozens of claimed proofs have failed scrutiny, and even the most significant recent development (the unverified challenge to ETH) stops far short of polynomial time.

For the more plausible quantum threat, Bitcoin has a credible draft path: BIP-360's P2MR outputs, phased signature migration, and Satoshi's original contingency for hash breakage. A true collapse of computational hardness would demand something far more radical than an incremental soft fork. Until the evidence changes, the existing model continues to function, and the sensible work is on the transition we can see coming.

## Sources
- [Clay Mathematics Institute - P vs NP](https://www.claymath.org/millennium/p-vs-np/)
- [Computational Complexity blog - Respect the P v NP Problem (June 2026)](https://blog.computationalcomplexity.org/2026/06/respect-p-v-np-problem.html)
- [PostQuantum - On Lean-verified Millennium Prize claims](https://postquantum.com/industry-news/aix-global-innovations-millennium-prize/)
- [HackerNoon - OpenAI and Anthropic Claim AI Has Disproved a 27-Year-Old Hypothesis](https://hackernoon.com/openai-and-anthropic-claim-ai-has-disproved-a-27-year-old-computer-science-hypothesis)
- [IBTimes - AI Hits Computer Science With a 27-Year Bombshell](https://www.ibtimes.sg/A000Otv)
- [Gizmodo - If You Solve This Math Problem, You Could Steal All the Bitcoin](https://gizmodo.com/if-you-solve-this-math-problem-you-could-steal-all-the-1836047131)
- [Medium - Bitcoin's Worst Nightmare Is a Unicorn (Knuth on non-constructive proofs)](https://medium.com/thecryptoelement/bitcoins-worst-nightmare-is-a-unicorn-bfa08ef06e0f)
- [BIP-360 specification (bitcoin/bips)](https://raw.githubusercontent.com/bitcoin/bips/master/bip-0360.mediawiki)
- [Bitcoin Magazine - Bitcoin Advances Toward Quantum Resistance with BIP 360](https://bitcoinmagazine.com/news/bitcoin-advances-toward-quantum-resistance)
- [Cointelegraph - What BIP-360 Changes and What It Does Not](https://cointelegraph.com/features/bitcoin-s-quantum-upgrade-path-what-bip-360-changes-and-what-it-does-not)
- [PostQuantum - Fixing Bitcoin: The Post-Quantum Migration Technical Roadmap](https://postquantum.com/quantum-threat-crypto/fixing-bitcoin-pqc-migration/)
