---
layout: post
title: "Arpil2024-BTC Wizardsardine's new Self Custody Wallet products Revault & Liana"
date: 2024-03-14 23:59:59 -0000
categories: btc multi-sig decay inheritance planning security self-custody
author: "Sagun Garg"
tags: btc multi-sig decay inheritance planning
---

Kevin delves into the technical intricacies of Wizard Sardine's two Bitcoin security products: Revault and Liana. These solutions aim to address the challenges of self-custody and provide advanced features for users seeking enhanced protection and control over their digital assets.

Revault is described as a practical Bitcoin vault architecture that enables users to set spending policies and limits on their Bitcoin holdings. Interestingly, Revault does not require the implementation of advanced features like covenants, which were previously considered necessary for building functional Bitcoin vaults. The key innovation of Revault lies in its ability to achieve this level of control and security without the need for such complex protocol-level changes.

He highlights the importance of Revault's design, which is centered around the use of pre-signed transactions. This approach allows users to set spending limits and restrictions without the requirement to pre-compute the exact amounts to be transferred. This flexibility is a significant advantage over earlier vault designs, which often faced the challenge of having to predefine all transaction details, leading to potential issues if the amount being sent did not match the pre-computed values.

In contrast, Liana is presented as a Bitcoin wallet focused on providing protection against the loss of funds, rather than defense against theft. Liana's key feature is the utilization of multi-signature setups combined with time-locked backup keys. This setup enables users to designate authorized individuals, such as family members or trusted third parties, to access the funds after a specified period of inactivity.

He delves into the various setup options available with Liana, including inheritance scenarios, safer backups, and expanding multi-signature configurations. The inheritance use case is particularly interesting, as it addresses the challenge of securely passing on Bitcoin holdings to beneficiaries without relying on trusted third-party custodians. Liana's time-locked backup keys provide a more self-sovereign solution, where the designated heirs can access the funds after a predetermined period of time, without the need for the original owner to be present.

He also discusses the trade-offs associated with Liana's design, such as the requirement to periodically refresh the time-locked keys to prevent the loss of funds. This need to maintain the system actively introduces a level of complexity that may be a barrier for some users. Additionally, He explores the technical challenges around displaying the Miniscript policies, which underlie the multi-signature setups, in a user-friendly manner.

The discussion extends to the potential benefits of Bitcoin soft forks, such as covenants and OP_VAULT, and how they could enhance the user experience of products like Revault and Liana. However, the speaker expresses caution regarding the proliferation of multiple competing covenant proposals, highlighting the potential long-term maintenance and support challenges that could arise.

Throughout Kevin places the emphasis on the practical, real-world implementations of these security solutions, rather than purely theoretical or speculative approaches. The speakers consistently emphasize the importance of building tools that work with the Bitcoin network as it exists today, rather than relying on hypothetical future capabilities.

In conclusion, this podcast offers a comprehensive technical overview of Wizard Sardine's Revault and Liana, delving into the nuanced design decisions, trade-offs, and potential future developments in the realm of advanced Bitcoin self-custody solutions. The depth of the technical discussion provides valuable insights for individuals and organizations seeking to better understand the evolving landscape of secure Bitcoin management.