### PhosPay Websocket Messaging & Transaction Management System (PhosPay-WS-MTMS / Phos-MTMS)

The design philosophy of PhosPay Websocket Messaging & Transaction Management System (PhosPay-WS-MTMS / Phos-MTMS) is to mimic the human network comprising Payor, Payee and Agents, facilitated by conventional electronic and physical means (e.g. telephone conversations, paper contracts, verbal contracts etc.) to coordinate the various stages of transactions.

As such, let us begin by considering a scenario WITHOUT Phos-MTMS, and creating a PROTOCOL amongst various parties (Payor, Payee and Agents etc.) facilitated by conventional electronic and physical means (e.g. telephone conversations, paper contracts, verbal contracts etc.) to coordinate the various stages of transactions.

Subsequently, we can then design Phos-WTMS to faciliate the transactions.

Some readers may object that there is not thing very clever in this strategy, or it does not deserve to be called "smart contract".

Our rebuttal is that smart contract is still an ill defined concept with poor implementations anyway. Although we may not be able to fully qualify PhosPay as smart contract according to the definitions of some readers, what we have described above are based on sound and verifiable principles. As such, they will serve at least as some useful development towards an ideal smart contract implementation, or in plain English, a step in the right direction.


#### An Ad Hoc Online Tipping System

Consider:
- [ Scenario I: PhosPay with Western Union ](https://github.com/udexon/PhosPay/blob/master/PhosPay_Scenarios.md#scenario-i-phospay-with-western-union)

- Scenario X-I (X="no PhosPay"): the human network comprising Payor, Payee and Agents, facilitated by conventional electronic and physical means (e.g. telephone conversations, paper contracts, verbal contracts etc.) to coordinate the various stages of transactions, to perform online tipping of USD 1.

<img src="https://github.com/udexon/DatongToken/blob/master/pay_wu.png" width="400"  />

More specifically, Agent C (Christ) and Agent D (Donald) are individuals not affiliated with Western Union.

We intentionally use this unrealistic example to make readers aware of various issues, such as the Western Union commission fees, which exceed the tip USD 1 itself.

Suppose we increase the tip to USD 20 to make it realistic, in comparison to the commission fees.

Suppose Payor A (Adam), Payee B (Brenda) and Agents Christ and Donald use a mixture of online chat and voice conversations to facilitate the transactions. The following will be the steps required:

1. Adam informs Brenda of his intention to tip her.

2. Brenda agrees and gives her account details to Adam.

3. Adam and Brenda search online to identify Agent C who would initiate sending money at Wester Union branch near in country P, and Agent D who would receive money from the Wester Union branch in country Q, then transfer the money to Brenda's account.

4. Once Agent C is identified, i.e. Christ, Adam transfers money online from his bank account to Christ's bank account, using national inter-bank transfer service, where both Adam and Christ reside in country P.

5. Christ goes to the nearest Western Union branch and transfer money to Donald.

6. Donald then obtains the money Western Union branch in country Q, then transfers the money to Brenda's bank account, using national inter-bank transfer service.
