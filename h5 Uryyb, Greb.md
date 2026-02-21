# Schneier (2015) Applied Cryptography

The basic concepts of cryptography by explaining how secure communication works between two parties. The main idea is that a sender wants to send information securely to a receiver so that unauthorized people cannot read or understand the message. Cryptography is the tools and methods that protect this communication. So the main goal of cryptography is to ensure that even if someone intercepts the message, they cannot understand it without proper authorization.

## Encryption and Decryption terms

+ Plaintext: The original readable message before any protection is applied.
+ Encryption: The process of converting plaintext into a secret form to hide its meaning.
+ Ciphertext: The encrypted message that appears unreadable to anyone without the correct key.
+ Decryption: The process of converting ciphertext back into readable plaintext.

So encryption protects the message during transmission, while decryption allows the receiver to recover the original content.

# Karvinen (2023): PGP

This article explains how to use PGP encryption with the GNU Privacy Guard (gpg) tool to send secure messages over an untrusted network such as the Internet.

+ First, I generated a PGP keypair using gpg --gen-key. The keypair consists of a public key and a private key. The public key can be shared with others, while the private key must remain secret. I verified the key creation using gpg --fingerprint.
<img width="829" height="550" alt="1" src="https://github.com/user-attachments/assets/4ead5ce4-48c8-48cc-8c21-4ff4bf21c453" />
+ Then I exported my public key using ASCII armor format so it can be easily shared through email or text.
<img width="737" height="507" alt="2" src="https://github.com/user-attachments/assets/d90fb8cf-934c-4ea7-b7d1-63189aab6e93" />

+ To simulate communication between two users, I created a separate directory representing another user (Alice). Using "gpg --homedir . --gen-key" stored keys separately.
+ Then imported my public key into alive to allow encryption toward me.
+ I wrote a message and encrypted using the recipient’s public key and signed using Alice’s private key.
+ Here I decrypted the message using my private key. "gpg --decrypt encrypted.pgp" also verified Alice’s signature using her public key that confirming the message had not been modified.
