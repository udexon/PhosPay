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

3. Adam then creates a message in JSON, expressing his intention to pay Brenda USD 1:

```JavaScript
Object { 
PBK: "-----BEGIN PUBLIC KEY-----\nMFwwDQYJKoZIhvcNAQEBBQADSwAwSAJBAI+8tIdw4aGhmrEl9yx6pNZ4gsMzAyzq\nQ/OFd75LdWLLxEmiCzEvrRVwokH1UtGBCb53USKFDo8l8aKRjexBX90CAwEAAQ==\n-----END PUBLIC KEY-----", 
ID: "Adam", 
guid: "C58A1FC5-3DD1-4BCD-A21E-DFA774A0DEAB", 
msg: "I shall pay you USD 1.", 
time: "2020-01-19T07:34:34.084Z" }
```

His message includes his own public key (PBKA, A=Adam), and additional flags.

This JSON message is encrypted using Brenda's public key (PBKB) and stored at a website accessible by Brenda:

https://github.com/udexon/PhosPay/blob/master/rsa002.txt

Adam then generate a short URL for the above and paste it as a social media comment on Brenda's social media's account.

4. Brenda retrieves the encrypted message and descrypts it with her own private key (PVKB).
