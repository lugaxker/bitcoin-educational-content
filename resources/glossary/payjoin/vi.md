---
term: PAYJOIN

---
A specific Bitcoin transaction structure that enhances user privacy during a spending by collaborating with the payment recipient. The uniqueness of Payjoin lies in its ability to generate a transaction that looks ordinary at first glance but is actually a mini coinjoin between two parties. For this, the transaction structure involves the payment recipient in the inputs alongside the actual sender. Thus, the recipient includes a payment to themselves in the middle of the transaction that allows them to be paid. For example, if you buy a baguette for `6,000 sats` using a UTXO of `10,000 sats`, and you opt for a Payjoin, your baker will add a UTXO of `15,000 sats` belonging to them as an input, which they will retrieve in full as an output, in addition to your `6,000 sats`.

The Payjoin transaction fulfills two objectives. Firstly, it aims to mislead an external observer by creating a decoy in the chain analysis on the Common Input Ownership Heuristic (CIOH). Usually, when a transaction on the blockchain has multiple inputs, it is presumed that all these inputs likely belong to the same entity. Thus, when an analyst examines a Payjoin transaction, they are led to believe that all inputs come from the same person. However, this perception is incorrect because the payment recipient also contributes to the inputs alongside the actual payer. Secondly, the Payjoin also deceives an external observer about the actual amount of the payment that was made. By examining the structure of the transaction, the analyst might believe that the payment is equivalent to the amount of one of the outputs. In reality, the payment amount corresponds to none of the outputs. It is actually the difference between the recipient's UTXO in the output and the recipient's UTXO in the input. In this, the Payjoin transaction falls into the realm of steganography. It allows hiding the actual amount of a transaction within a false transaction that acts as a decoy.

![](../../dictionnaire/assets/14.webp)

> ► *Payjoin is also sometimes called "P2EP (Pay-to-End-Point)", "Stowaway", or "steganographic transaction".*