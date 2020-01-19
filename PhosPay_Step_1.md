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

Brenda then copies her public key (PBKB) to her Facebook page, or any other social media page. She may renew her public key from time to time. A public key needs to be used only for one transaction. This is one of the most crucial innovation in PhosPay.

<img src="https://github.com/udexon/PhosPay/blob/master/PhosPay_Demo/Brenda_FB.png" width=300>

