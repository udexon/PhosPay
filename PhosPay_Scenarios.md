### PhosPay Online Tipping &ndash; Outside China &ndash; 大同支外宝

Online tipping is one of the most lucrative captive markets nowadays. China and users of Chinese apps are ahead of the rest of the world in this area with their online payment systems which enables tipping down to a single cent. Just like HTML and Linux, something small and simple can replicate worldwide and become revolutionary.

https://en.wikipedia.org/wiki/Software_token

#### Scenario I: PhosPay with Western Union

<img src="https://github.com/udexon/DatongToken/blob/master/pay_wu.png" width="400"  />

Scenario I involves an international conventional payment method (Western Union) without cryptocurrency so that users can confirm that PhosPay Token can be used without cryptocurrency.

Consider a scenario where Sender A who lives in country P wishes to send an amount X in currency K to Recipient B who lives in country Q.

Step 1: Verifying payment chain (identifying Agents)

<img src="https://github.com/udexon/DatongToken/blob/master/payment_chain.png" width="400"  />

<ol type="a">
  <li> Sender A wishes to tip Recipient B. A leaves a comment on B's social media post (Facebook, Instagram, YouTube, etc.) comprising a short link to A's PhosPay Token, together with the tipping amount, as well as other details. </li>
  
  <li> Sender A retrieves Recipient B's public key PBKB from B's social media profile or posts. </li>

  <li> Sender A first encrypt a raw message MA1 with own public key PBKA as encrypted messages CA1. </li>
  <li> Sender A then encrypt encrypted message CA1 with Recipient B's public key PBKB as encrypted message CA2.</li>
  <li> Sender A leaves CA2 on a website accessible by B and post the short URL on Recipient B's social media. </li>
  <li> Recipient B then opens the short link using PhosPay app decrypts CA2 using own private key PVKB. B begins a chat session with A. </li>

<li> Sender A must include own public key in payment token, so that Recipient B can encrypt message MB and send it to Agent D, who lives in the same country Q as B. </li>

<li> Then Agent D can send an encrypted message to Agent C, who lives in the same country P as Sender A, to verify payment. </li>

<li> Agent C then sends message CA1 back to Sender A, who then decrypts CA1 to verify that Agent C obtained CA1 via a chain of agents from Recipient B. </li>
</ol>

Jump to: 
- [ A more detailed implementations of steps (a) to (f) ](https://github.com/udexon/PhosPay/blob/master/PhosPay_Step_1.md)
- [ An ID-less Websocket Messaging and Transaction Management System \[ steps (g) to (i) \] ](https://github.com/udexon/PhosPay/blob/master/PhosPay_WS_TMS.md)

Step 2: Carry out payment transactions

<img src="https://github.com/udexon/DatongToken/blob/master/pay_wu.png" width="400"  />

- Once the payment chain is verified, Agent C may collect cash from Sender A physically or use the national banking system in country P to collect the payment. 
- Agent C will pay Agent D using their own international payment method. 
- Agent D can then pay Recipient B cash physically in person, or using the national banking system in country Q.


#### Scenario II: PhosPay with Cryptocurrency

Now consider this variation:

-- Agent C sends money using cryptocurrency L to Agent D.

<img src="https://github.com/udexon/DatongToken/blob/master/pay_bch.png" width="400"  />

### Novel Applications of Public Key Encryption


Let's illustrate the two scenarios in diagrams:

<img src="https://github.com/udexon/DatongToken/blob/master/pay_wu.png" width="400"  />

<img src="https://github.com/udexon/DatongToken/blob/master/pay_bch.png" width="400"  />

We now have sufficient understanding to compare and analyse various fundamental issues concerning international financial transactions, cryptocurrencies and PhosPay Token.



- From the technical perspective, what are the roles of RSA in both scenarios?

Firstly, as with Bitcoin, we use RSA cryptosystem to authenticate the users (Sender, Recipient, Agents). 

However, in Bitcoin, after the sender and recipient identities are authenticated, the programs concerned automatically carry out a series of operations to deduct the balance from the wallet of the sender and add the exact same amount in the recipient's wallet (which can be either in software or hardware).


https://en.bitcoin.it/wiki/Transaction

In PhosPay, it is the human users (Sender, Recipient, Agents) who will perform the operations as specified in the token.

- Minimizing agent fees

PhosPay network would have many agents in each country, so that they would compete with each other to lower their commission fees.

As a result, agents using cryptocurrencies will have much greater demand for international money transfer, which in turn improve the adoption of cryptocurrencies.




#### (Non)-Adoption of Cryptocurrencies

PhosPay immediately solves the adoption problem of cryptocurrencies. Conventionally, the sender and the recipient both have to create a personal account for the cryptocurrency concerned. This has become the biggest obstacle for users to adopt cryptocurrencies as well as any transactional systems. 

In PhosPay Token, the mechanisms involved in a cryptocurrency transaction are broken down to the bare minimum. In the scenario described above for payment using PhosPay Token, the sender and recipient do not need to create personal accounts on PhosPay system, as the public key (and private key) or each user can be generated randomly at anytime. This fundamentally change the understanding of identity and communications.



#### Summary

Consider a simple act of tipping an Instamgrammer in Vietnam using PhosPay.

Sender A indicates his (her) wish to tip Recipient B, by leaving a comment on B's social media post (Facebook, Instagram, YouTube, etc.) comprising a short link to A's PhosPay Token, together with the tipping amount, as well as other details. A may also send the initial short link and meesages via a private chat app such as WhatsApp.

B then opens the short link using PhosPay app and begins a chat session with A. Sender A then requests Recipient B's public key.

After Sender A sends the token to Recipient B, presumably via a mobile chat service such as WhatsApp, Sender B will use a PhosPay app to process then token, then send a new token to Agent C. Agent C again will use a PhosPay app to process the token, and send a new token to Agent D. Agent D will also use a PhosPay app to process the token, and send a new token to Sender A.

All the transmissions of token can be done by sending text messages on chat apps like WhatsApp.

Finally, Sender A will use a PhosPay app to verify the token from Agent C, to confirm that Agent C is an authorized agent who will send money via conventional means to Agent D, and Agent D will send money via conventional means to Recipient B. After this confirmation, Sender A may send money to Agent C via conventional means, to initiate the transaction. 



