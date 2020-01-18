### PhosPay: Phos Payment Protocol

Smart contract, like codeless and serverless, seems to be an over-hyped snake oil, where their open source implementations are far lagging behind "expectations", or downright poorly documented.

PhosPay might just be the most definitive implementation of smart contract, as our implementation and documentation are designed to be verified by peers and adopted by collaborators.  As such, we hope that PhosPay may redefine the roadmaps of future smart contract implementations.

In [ Datong Token Online Tipping ](https://github.com/udexon/EMYL/blob/master/E003_Online_Tipping.md), which we shall rename as PhosPay, we describe an online tipping scheme based on ID-less asymetric cryptography. Based on the concepts described above, we describe an entity called PhosPay Wallet or PhosWallet, which accumulates the tipping amount on behalf of the Payee, before the Payee is even notified of the credits the Payee is eligible to claim.

Likewise, a Payor does not need to make physical or electronic payments to a PhosPay Agent, before the Payor's intention to pay the Payee of a certain amount X in currency P (including cryptocurrencies), is recorded in the Payor's PhosWallet.

As such, PhosPay acts as a smart contract, in the sense that it expresses the intention of the Payee to pay the Payor of a certain amount X in currency P, just like a conventional paper contract does.


#### Verifying Our Proposal

Conventional open source projects labelled as "smart contract" either:
- do not have a realistic short term goal (e.g. within 3 months), or 
- too few people understand the theories and proposals for implementations.
