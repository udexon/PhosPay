1. The first step in a PhosPay transaction consists of the following:
- Payor Adam indicates his wish to pay Payee Brenda USD 1, by sending a encrypted message to Brenda, using Brenda's public key.
- As such, Brenda must publish her public key on her social media post, so that Adam or anyone else who wishes to tip her, may use her public key for PhosPay transaction.

2. Brenda uses a PhosPay app to generate her public and private key pairs. As PhosPay is now still in development, we use a web based prototype to demonstrate the functions required.

<img src="https://github.com/udexon/PhosPay/blob/master/PhosPay_Demo/Brenda_PBK.png" width=700>

Brenda opens the PhosPay demo page at:

http://localhost/2020/node_clientname/phos_client.html

She then enters the following commands in the browser console:

```JavaScript
F("exkey:")   // export key: Phos stack machine returns Brenda's public key, pushed on to stack
S             // show stack i.e. Brenda's public key
```

Brenda then copies her public key (PBKB, B=Brenda) to her Facebook page, or any other social media page. She may renew her public key from time to time. A public key needs to be used only for one transaction. This is one of the most crucial innovation in PhosPay.

<img src="https://github.com/udexon/PhosPay/blob/master/PhosPay_Demo/Brenda_FB.png" width=300>

3. Adam then creates a message `MA` in JSON, expressing his intention to pay Brenda USD 1:

```JavaScript
Object { 
PBK: "-----BEGIN PUBLIC KEY-----\nMFwwDQYJKoZIhvcNAQEBBQADSwAwSAJBAI+8tIdw4aGhmrEl9yx6pNZ4gsMzAyzq\nQ/OFd75LdWLLxEmiCzEvrRVwokH1UtGBCb53USKFDo8l8aKRjexBX90CAwEAAQ==\n-----END PUBLIC KEY-----", 
ID: "Adam", 
guid: "C58A1FC5-3DD1-4BCD-A21E-DFA774A0DEAB", 
msg: "I shall pay you USD 1.", 
time: "2020-01-19T07:34:34.084Z" }
```

His message includes his own public key (PBKA, A=Adam), and additional flags.

The following commands are executed in Adam's PhosPay web client console:

```JavaScript
// push Brenda's public key PBKB on to stack
S.push("-----BEGIN PUBLIC KEY-----\nMFwwDQYJKoZIhvcNAQEBBQADSwAwSAJBAJ+hnkgPA59lIBsuFr3LT/de09/Y8MEc\nCKjsPF2fgLo3Bi5PlCTttvUeprhNj2Lx9Yublc6yR6GidPUWfbA+TkUCAwEAAQ==\n-----END PUBLIC KEY-----")
F("imkey:") // import PBKB to node-rsa
S.push(MA)  // push MA on to stack
F("je: ecr:")  // json encode MA; encrypt it;
S
```

<img src="https://github.com/udexon/PhosPay/blob/master/PhosPay_Demo/step_d_imkey.png" width=700>

<img src="https://github.com/udexon/PhosPay/blob/master/PhosPay_Demo/step_d_ecr.png" width=700>


This JSON message is encrypted using Brenda's public key (PBKB) and stored at a website accessible by Brenda:

https://github.com/udexon/PhosPay/blob/master/rsa002.txt

Adam then generates a short URL for the above and paste it as a social media comment on Brenda's social media's account.

4. Brenda retrieves the encrypted message and descrypts it with her own private key (PVKB):

```JavaScript
F("dcr:")
S
```

<img src="https://github.com/udexon/PhosPay/blob/master/PhosPay_Demo/step_e_CA2.png" width=700>

<img src="https://github.com/udexon/PhosPay/blob/master/PhosPay_Demo/step_f_dcr.png" width=700>


5. As we can see, the above constitute only the first step of PhosPay transaction.

Further steps are described in [PhosPay Online Tipping](https://github.com/udexon/PhosPay/blob/master/PhosPay_Scenarios.md) involving Agent C and Agent D in different countries, where the transactions will be managed using PhosPay Websocket Transaction Management System.

Jump to: [PhosPay Websocket Messaging & Transaction Management System](https://github.com/udexon/PhosPay/blob/master/PhosPay_WS_MTMS.md)
