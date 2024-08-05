---
term: FIBRE
---

Acronym for "*Fast Internet Bitcoin Relay Engine*". It is a protocol designed by Matt Corallo in 2016 to speed up the distribution of Bitcoin blocks across the globe. Its goal was to reduce propagation delays as close to physical limits as possible. FIBRE aimed to ensure a more equitable distribution of mining opportunities, by making sure that the proportion of blocks mined by a participant accurately reflects their contribution in terms of computing power, regardless of their position in the network.

Indeed, latency in block transmission can favor large, well-connected mining groups, often located close to each other, to the detriment of smaller ones. This phenomenon could, over time, increase the centralization of mining and reduce the overall security of the system. To address this issue, FIBRE introduced error correction codes and the transmission of additional data to counterbalance packet loss, as well as the use of compact blocks similar to those described in BIP152, all operating via UDP to bypass certain TCP limitations. Nonetheless, FIBRE was abandoned in 2020, mainly due to its dependence on a single maintainer and the fact that the adoption of BIP152 made such a system less essential.
