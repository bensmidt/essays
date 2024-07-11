Physical money is irrelevant. With online banking and the increasing popularity of E-wallets (Cash App, Paypal, Venmo), carrying cash is a hassle. Digital money, with its unparalleled convenience, will soon render cash obsolete. 

However, digital currency, with all its novelty, is messy. Government-backed fiat currency (paper money such as the dollar or the euro) is almost exclusively digital (92% of currency in the world is digital). The rise of cryptocurrency complicated digital currency by offering a fresh alternative: decentralized money.  

It’s difficult to accept. Money without authority is like candy with no wrapper. Questions besiege cryptocurrency from all sides. Where does it come from? Who controls it? What does it mean to “own” cryptocurrency? How do you even buy cryptocurrency?  

Bitcoin, cryptocurrency gold, has weathered attackers for twelve years now and aspires to be the world’s default currency. I didn’t write this article to speculate about 
Bitcoin’s future though. You can decide that for yourself. 

Rather, I want to provide a basic framework for what Bitcoin is and how it works. By the end of this article, you’ll have a solid conceptual understanding of Bitcoin. 

Before tackling Bitcoin though, understanding our current banking system is a helpful, if not essential, reference point. I wrote this separate five-minute article for you to use (since this article has so much information already). If you don’t have the time to read it, you should still understand Bitcoin, although I can’t make any promises.

If you’re confident in your understanding (or simply don’t have the time), here’s the article’s main idea: digital assets are easily replicated leading to the double spend problem (spending the same digital currency twice); banks solve this issue by acting as centralized bookkeepers between all transactions, ensuring nobody double-spends their digital money. 

Cryptography
------------
With bank payments understood, we just need a few vocabulary words from the world of cryptography to plunge into the world of Bitcoin.

Hash Functions
--------------
Hash functions sound fancy (and they definitely can be) but conceptually they’re very simple. A hash function is a series of mathematical steps performed on an input (text) to produce an output, known as a hash value. If you’ve ever heard of SHA-256 or MD5, these are hash functions. 
 
Under the umbrella of hash functions is a cryptographic hash function, which is what Bitcoin uses. It’s the same general concept but more specific in that it has these five properties: 
1.	The same message always produces the same hash value
2.	The hash function quickly computes any given message
3.	You cannot return from the hash value to the original text 
4.	A small change in the message produces a large change in the hash value
5.	It’s extremely difficult to create the same hash value out of two different messages

For emphasis, cryptographic hash functions are one-way (rule 3). The only way to obtain the original text from a hash value is by inputting possible messages until the hash function produces the same hash value (rule 1). As you can guess, this highly improbable and remarkably time-consuming. 

Digital Signatures
------------------
You’ve likely heard of encryption and decryption. Encryption is when you use a key to convert plaintext (readable text) into ciphertext (encoded, unreadable text). The same key can then be used to convert the ciphertext back into plaintext (decryption). This process uses a symmetric cipher, meaning the key to encrypt and decrypt text is the same. 

Symmetric Encryption 
--------------------
However, an asymmetric cipher, which uses two different keys, is superior for Bitcoin. An asymmetric cipher has a private key and a public key, which are uniquely linked with fancy math. Your private key, as the name suggests, should never be shared. Your public key is free to be known by all though. Together the two form a key pair. 
Bitcoin uses digital signatures, a type of asymmetric cipher, which allows you to securely sign a document (digitally of course) with your private key. The public can then verify your signature with your public key. Let’s see how this works. 
 
You begin by using your private key (only known by you) along with the message you’re signing to create your digitally signed document. Powered by some fancy math, only your public (which is uniquely linked to your private key) can decrypt the text. 
As such, anyone can use your public key to validate that your encrypted message was created using your private key. If your private key wasn’t used or a public key that isn’t yours is used to verify the encryption, it will return false. 

Digital Signatures Using Asymmetric Encryption
----------------------------------------------

It’s important to remember that the private key encryption depends on the message it's encrypting. Changing even 1 character of the message significantly alters the encryption. As a result, the only manner in which two separate encryptions can be the same is if the exact same message with the exact same private key is used. Otherwise, all encryptions created with a private key are unique (but still verifiable) since each message is different. 

Whew! I know that was a lot to digest but you’ll soon understand why all this information is necessary. If you want, feel free to take a quick bathroom break or grab a drink of water, and then we’ll get o what you’re really here for.

Creating Decentralized Currency 
-------------------------------
Glad you’re back! With all this prerequisite knowledge under our belts, it’s time to dive into how Satoshi Nakamoto built the decentralized currency of Bitcoin. By the way, Satoshi Nakamoto is a pseudonym (fake name). No one knows the true identity of Bitcoin’s creator…
Anyways, let’s begin by going back to our bookeeping
