---
term: BIP68

---
Introduced the ability to use relative lock-times through the `nSequence` field. This allows a transaction to specify a relative delay before it can be included in a block. This delay can be defined in terms of the number of blocks, or as a multiple of 512 seconds (i.e., real time). Note that this new interpretation of the `nSequence` field is only valid if the `nVersion` field is greater than or equal to `2`. This interpretation of the `nSequence` field occurs at the level of Bitcoin's consensus rules. The relative timelock sets a delay starting from the acceptance of a previous transaction, while the absolute timelock specifies a precise moment before which the transaction cannot be included in a block. BIP68 was introduced via a soft fork on July 4, 2016, alongside BIP112 and BIP113, activated for the first time using the BIP9 method.